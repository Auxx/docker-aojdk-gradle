FROM adoptopenjdk/openjdk11:alpine

ENV GRADLE_VERSION=5.3
ENV GRADLE_HOME=/opt/gradle

ARG gradle_user_home=/opt/project/.gradle_home
ENV GRADLE_USER_HOME=$gradle_user_home

RUN set -o errexit -o nounset \
  && wget --no-verbose "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip" \
  && mkdir "${GRADLE_HOME}" \
  && unzip -d "${GRADLE_HOME}" "gradle-${GRADLE_VERSION}-bin.zip" \
  && rm -f "gradle-${GRADLE_VERSION}-bin.zip" \
  && ln -s "${GRADLE_HOME}/gradle-${GRADLE_VERSION}/bin/gradle" /usr/bin/gradle

RUN set -o errexit -o nounset \
  && echo "Testing installation..." \
  && gradle --version
