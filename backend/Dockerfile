#
# Licensed to the Apache Software Foundation (ASF) under one
# or more contributor license agreements.  See the NOTICE file
# distributed with this work for additional information
# regarding copyright ownership.  The ASF licenses this file
# to you under the Apache License, Version 2.0 (the
# "License"); you may not use this file except in compliance
# with the License.  You may obtain a copy of the License at
#
#   http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing,
# software distributed under the License is distributed on an
# "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
# KIND, either express or implied.  See the License for the
# specific language governing permissions and limitations
# under the License.
#
FROM  openjdk:8-jdk-oracle

ENV JAVA_MEM_OPTS="-Xmx1024m -Xms1024m -XX:MetaspaceSize=256m -XX:MaxMetaspaceSize=256m"

COPY  target/*.jar /app/app.jar

RUN mkdir /data

EXPOSE 9090

ENTRYPOINT ["java", "-jar", "${JAVA_MEM_OPTS}","/app/app.jar"]
