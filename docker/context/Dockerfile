#
# Copyright 2020 Tom van den Berg (TNO, The Netherlands).
# SPDX-License-Identifier: Apache-2.0
#

FROM tomcat:9-jre8

ARG VERSION

# Use brute the force to set webview as default
RUN rm -rf $CATALINA_HOME/webapps/ROOT $CATALINA_HOME/webapps/ROOT.war

COPY webview-${VERSION}.war $CATALINA_HOME/webapps/ROOT.war

# Expose default HTTP port
EXPOSE 8080
