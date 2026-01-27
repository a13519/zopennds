cmake_minimum_required(VERSION 4.1)
project(zousysopennds)

set(CMAKE_CXX_STANDARD 14)

include_directories(files)
include_directories(files/etc)
include_directories(files/usr)
include_directories(src)

add_executable(zousysopennds
        files/etc/config/opennds
        files/etc/init.d/opennds
        files/etc/uci-defaults/40_opennds
        files/usr/lib/opennds/restart.sh
        src/auth.c
        src/auth.h
        src/client_list.c
        src/client_list.h
        src/commandline.c
        src/commandline.h
        src/common.h
        src/conf.c
        src/conf.h
        src/debug.c
        src/debug.h
        src/fw_iptables.c
        src/fw_iptables.h
        src/http_microhttpd.c
        src/http_microhttpd.h
        src/http_microhttpd_utils.c
        src/http_microhttpd_utils.h
        src/main.c
        src/main.h
        src/mimetypes.h
        src/ndsctl.c
        src/ndsctl.h
        src/ndsctl_thread.c
        src/ndsctl_thread.h
        src/safe.c
        src/safe.h
        src/util.c
        src/util.h)
