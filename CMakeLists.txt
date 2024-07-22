cmake_minimum_required(VERSION 3.16)

project(kwin-effect-reflectcursor)
set(PROJECT_VERSION "0.1")
SET(PROJECT_VERSION_MAJOR 0)

set(QT_MIN_VERSION "6.6.0")
set(KF_MIN_VERSION "5.248.0")
set(KDE_COMPILERSETTINGS_LEVEL "5.82")

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

include(FeatureSummary)

find_package(ECM ${KF_MIN_VERSION} REQUIRED NO_MODULE)
set(CMAKE_MODULE_PATH ${ECM_MODULE_PATH})

include(KDEInstallDirs)
include(KDECMakeSettings)
include(KDECompilerSettings NO_POLICY_SCOPE)

find_package(Qt6 ${QT_MIN_VERSION} REQUIRED COMPONENTS Widgets)
find_package(KF6 ${KF_MIN_VERSION} REQUIRED COMPONENTS Config)
find_package(KWin REQUIRED)

kcoreaddons_add_plugin(reflectcursor INSTALL_NAMESPACE "kwin/effects/plugins")

target_compile_definitions(reflectcursor PRIVATE -DTRANSLATION_DOMAIN=\"effect_reflectcusor\")

target_sources(reflectcursor PRIVATE
    main.cpp
    reflectcursor.cpp
)

kconfig_add_kcfg_files(reflectcursor
    reflectcursorconfig.kcfgc
)

target_link_libraries(reflectcursor PRIVATE
    KF6::ConfigGui

    KWin::kwin
)
