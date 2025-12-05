if( IOS OR ANDROID OR NOT PLATEAU_USE_FBX)
  # iOS/Android または FBX無効時はダミー実装を使用
  target_sources(plateau PRIVATE
      "obj_writer.cpp"
      "gltf_writer.cpp"
      "fbx_writer_dummy.cpp"
    )
else()
  # デスクトップ環境でFBX有効時
  target_sources(plateau PRIVATE
      "obj_writer.cpp"
      "gltf_writer.cpp"
      "fbx_writer.cpp"
    )
endif()
