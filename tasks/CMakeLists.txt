# Generated from orogen/lib/orogen/templates/tasks/CMakeLists.txt

include(occlusion_inpaintingTaskLib)
ADD_LIBRARY(${OCCLUSION_INPAINTING_TASKLIB_NAME} SHARED
    ${OCCLUSION_INPAINTING_TASKLIB_SOURCES})
add_dependencies(${OCCLUSION_INPAINTING_TASKLIB_NAME}
    regen-typekit)


TARGET_LINK_LIBRARIES(${OCCLUSION_INPAINTING_TASKLIB_NAME}
    ${OrocosRTT_LIBRARIES}
    ${QT_LIBRARIES}
    ${OCCLUSION_INPAINTING_TASKLIB_DEPENDENT_LIBRARIES})
SET_TARGET_PROPERTIES(${OCCLUSION_INPAINTING_TASKLIB_NAME}
    PROPERTIES LINK_INTERFACE_LIBRARIES "${OCCLUSION_INPAINTING_TASKLIB_INTERFACE_LIBRARIES}")
SET_TARGET_PROPERTIES(${OCCLUSION_INPAINTING_TASKLIB_NAME}
    PROPERTIES INTERFACE_LINK_LIBRARIES "${OCCLUSION_INPAINTING_TASKLIB_INTERFACE_LIBRARIES}")

INSTALL(TARGETS ${OCCLUSION_INPAINTING_TASKLIB_NAME}
    RUNTIME DESTINATION bin
    LIBRARY DESTINATION lib/orocos)

INSTALL(FILES ${OCCLUSION_INPAINTING_TASKLIB_HEADERS}
    DESTINATION include/orocos/occlusion_inpainting)

