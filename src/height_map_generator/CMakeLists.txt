# モバイル向けはlibpng依存のためスキップ（heightmap_generator.cppがpng.hをinclude）
if (NOT(IOS OR ANDROID))
    target_sources(plateau PRIVATE
            "heightmap_generator.cpp"
            "heightmap_mesh_generator.cpp"
            "heightmap_with_alpha.cpp"
            "heightmap_operation.cpp"
    )
endif()
