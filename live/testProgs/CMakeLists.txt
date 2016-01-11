# CMakeLists.txt testProgs directory

# headers
SET(COMMON_HDRS
	playCommon.hh
)

SET(COMMON_LIBS
	BasicUsageEnvironment
	groupsock
	liveMedia
	UsageEnvironment
	BasicUsageEnvironment
)

ADD_EXECUTABLE(openRTSP openRTSP.cpp playCommon.cpp ${COMMON_HDRS})
TARGET_LINK_LIBRARIES(openRTSP ${COMMON_LIBS} ${EXTRA_LIBS})

ADD_EXECUTABLE(playSip playSIP.cpp playCommon.cpp ${COMMON_HDRS})
TARGET_LINK_LIBRARIES(playSip ${COMMON_LIBS} ${EXTRA_LIBS})

ADD_EXECUTABLE(testAmrAudioStreamer testAMRAudioStreamer.cpp ${COMMON_HDRS})
TARGET_LINK_LIBRARIES(testAmrAudioStreamer ${COMMON_LIBS} ${EXTRA_LIBS})

ADD_EXECUTABLE(testH264VideoStreamer testH264VideoStreamer.cpp ${COMMON_HDRS})
TARGET_LINK_LIBRARIES(testH264VideoStreamer ${COMMON_LIBS} ${EXTRA_LIBS})

ADD_EXECUTABLE(testH265VideoStreamer testH265VideoStreamer.cpp ${COMMON_HDRS})
TARGET_LINK_LIBRARIES(testH265VideoStreamer ${COMMON_LIBS} ${EXTRA_LIBS})

ADD_EXECUTABLE(testOnDemandRTSPServer testOnDemandRTSPServer.cpp ${COMMON_HDRS} )
TARGET_LINK_LIBRARIES(testOnDemandRTSPServer ${COMMON_LIBS} ${EXTRA_LIBS})

ADD_EXECUTABLE(testRTSPClient testRTSPClient.cpp ${COMMON_HDRS})
TARGET_LINK_LIBRARIES(testRTSPClient ${COMMON_LIBS} ${EXTRA_LIBS})

ADD_EXECUTABLE(testMPEG2TransportStreamer testMPEG2TransportStreamer.cpp ${COMMON_HDRS})
TARGET_LINK_LIBRARIES(testMPEG2TransportStreamer ${COMMON_LIBS} ${EXTRA_LIBS})
