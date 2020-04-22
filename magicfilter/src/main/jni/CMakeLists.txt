

cmake_minimum_required(VERSION 3.4.1)

add_library(MagicBeautify

             SHARED

             ./MagicJni.cpp
             ./beautify/MagicBeautify.cpp
             ./beautify/MagicBeautify.h
             ./bitmap/BitmapOperation.cpp
             ./bitmap/BitmapOperation.h
             ./bitmap/Conversion.cpp
             ./bitmap/Conversion.h
             ./bitmap/JniBitmap.h )


find_library(log-lib
              log )

find_library(jnigraphics-lib
        jnigraphics)

target_link_libraries(MagicBeautify
                       ${log-lib}
                       ${jnigraphics-lib})
