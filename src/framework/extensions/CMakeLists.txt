# SPDX-License-Identifier: GPL-3.0-only
# MuseScore-CLA-applies
#
# MuseScore
# Music Composition & Notation
#
# Copyright (C) 2021 MuseScore BVBA and others
#
# This program is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License version 3 as
# published by the Free Software Foundation.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program.  If not, see <https://www.gnu.org/licenses/>.

set(MODULE extensions)

include(${CMAKE_CURRENT_LIST_DIR}/api/v1/apiv1.cmake)

set(MODULE_SRC
    ${CMAKE_CURRENT_LIST_DIR}/extensionsmodule.cpp
    ${CMAKE_CURRENT_LIST_DIR}/extensionsmodule.h
    ${CMAKE_CURRENT_LIST_DIR}/extensionstypes.h
    ${CMAKE_CURRENT_LIST_DIR}/iextensionsprovider.h
    ${CMAKE_CURRENT_LIST_DIR}/iextensionsconfiguration.h
    ${CMAKE_CURRENT_LIST_DIR}/iextensionsuiengine.h

    ${CMAKE_CURRENT_LIST_DIR}/api/qmlextapi.cpp
    ${CMAKE_CURRENT_LIST_DIR}/api/qmlextapi.h
    ${CMAKE_CURRENT_LIST_DIR}/api/scriptapi.cpp
    ${CMAKE_CURRENT_LIST_DIR}/api/scriptapi.h
    ${CMAKE_CURRENT_LIST_DIR}/api/qmllistproperty.h
    ${API_V1_SRC}

    ${CMAKE_CURRENT_LIST_DIR}/internal/extensionsprovider.cpp
    ${CMAKE_CURRENT_LIST_DIR}/internal/extensionsprovider.h
    ${CMAKE_CURRENT_LIST_DIR}/internal/extensionsconfiguration.cpp
    ${CMAKE_CURRENT_LIST_DIR}/internal/extensionsconfiguration.h
    ${CMAKE_CURRENT_LIST_DIR}/internal/extensionsloader.cpp
    ${CMAKE_CURRENT_LIST_DIR}/internal/extensionsloader.h
    ${CMAKE_CURRENT_LIST_DIR}/internal/extensionrunner.cpp
    ${CMAKE_CURRENT_LIST_DIR}/internal/extensionrunner.h
    ${CMAKE_CURRENT_LIST_DIR}/internal/scriptengine.cpp
    ${CMAKE_CURRENT_LIST_DIR}/internal/scriptengine.h
    ${CMAKE_CURRENT_LIST_DIR}/internal/jsmoduleloader.cpp
    ${CMAKE_CURRENT_LIST_DIR}/internal/jsmoduleloader.h
    ${CMAKE_CURRENT_LIST_DIR}/internal/extensionsuiactions.cpp
    ${CMAKE_CURRENT_LIST_DIR}/internal/extensionsuiactions.h
    ${CMAKE_CURRENT_LIST_DIR}/internal/extensionsactioncontroller.cpp
    ${CMAKE_CURRENT_LIST_DIR}/internal/extensionsactioncontroller.h

    ${CMAKE_CURRENT_LIST_DIR}/internal/legacy/extpluginsloader.cpp
    ${CMAKE_CURRENT_LIST_DIR}/internal/legacy/extpluginsloader.h
    ${CMAKE_CURRENT_LIST_DIR}/internal/legacy/extpluginrunner.cpp
    ${CMAKE_CURRENT_LIST_DIR}/internal/legacy/extpluginrunner.h

    ${CMAKE_CURRENT_LIST_DIR}/view/extensionbuilder.cpp
    ${CMAKE_CURRENT_LIST_DIR}/view/extensionbuilder.h
    ${CMAKE_CURRENT_LIST_DIR}/view/extensionsuiengine.cpp
    ${CMAKE_CURRENT_LIST_DIR}/view/extensionsuiengine.h
    ${CMAKE_CURRENT_LIST_DIR}/view/extensionsmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/view/extensionsmodel.h

    ${CMAKE_CURRENT_LIST_DIR}/devtools/devextensionslistmodel.cpp
    ${CMAKE_CURRENT_LIST_DIR}/devtools/devextensionslistmodel.h
    )

set(MODULE_QRC extensions.qrc)

set(MODULE_QML_IMPORT ${CMAKE_CURRENT_LIST_DIR}/qml )

include(SetupModule)


