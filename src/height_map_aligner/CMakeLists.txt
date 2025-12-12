# モバイル向けはheight_map_generator依存のためスキップ
if (NOT(IOS OR ANDROID))
    target_sources(plateau PRIVATE
        "height_map_aligner.cpp"
        "open_mesh_converter.cpp"
    )
endif()
