cmake_minimum_required(VERSION 3.16)
project(gladVK)

# Add the GLAD library
add_library(gladVK STATIC
	"include/vk_platform.h"
	"include/glad/vulkan.h"
	"include/vk_video/vulkan_video_codec_av1std.h"
	"include/vk_video/vulkan_video_codec_av1std_decode.h"
	"include/vk_video/vulkan_video_codec_h264std.h"
	"include/vk_video/vulkan_video_codec_h264std_decode.h"
	"include/vk_video/vulkan_video_codec_h264std_encode.h"
	"include/vk_video/vulkan_video_codec_h265std.h"
	"include/vk_video/vulkan_video_codec_h265std_decode.h"
	"include/vk_video/vulkan_video_codec_h265std_encode.h"
	"include/vk_video/vulkan_video_codecs_common.h"
	"src/vulkan.c"
)

# Specify the include directories for GLAD
target_include_directories(gladVK PUBLIC
	${CMAKE_CURRENT_SOURCE_DIR}/include
)
