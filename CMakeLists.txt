cmake_minimum_required(VERSION 3.4.1)#说明要求的cmake最低版本
add_library( #这里三行从上往下看分别是生成库名称，生成库类型，源文件
               abc
               SHARED
               src/main/jni/Chello.c)
find_library( #这里是找到两个库
              log-lib
              log)
target_link_libraries( #这里链接了我们上面生成的库
                      abc
                      ${log-lib})