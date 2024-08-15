## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:9d3d9e1bbedb5c90e1b5b491a33af56ad9715cc8eadba71d8728d0536d084fd0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ibmjava:sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:51e52c510944da071b281454df91962099528cceb04a9237f59116445ed084ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.8 MB (100797743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d62acc3dbeee9514cc0697939681f5fa1edf0702de53b5c79a5096cc769a71e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 07:06:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Aug 2024 07:06:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_VERSION=8.0.8.30
# Thu, 15 Aug 2024 07:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='07df7f73c1ab08ca8adcfede1d35789fb36368d42226c32b998c36b84ace8aff';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='35bd6696ddb4a2ab54afc517efdd37ce3471cba589ebbcaad04019caec773510';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='32040e63bbf94b7a6e97ebcf28e4ba4c336c82b2e1c1131658e5762c82c204d7';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='11ee2b25766e7c4685f2f2a89f3bf54265a97c8ae52bcddd3a46a21e872ea436';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f762c3aa5f7bd9957cc6e7a5d97c7808fb2905b0183566b6e141bf65cc5212`  
		Last Modified: Thu, 15 Aug 2024 17:59:00 GMT  
		Size: 1.4 MB (1438244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2de647923e029983d9c2ae0295a588da74703d0f7e1ed3a1bbaefd095fc34d7`  
		Last Modified: Thu, 15 Aug 2024 17:59:02 GMT  
		Size: 69.8 MB (69825444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:6056de356b0a75ef8b429d050fa3f70aca362d8c92e83e407c8b13e43096262b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2027450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5772f05e8c5ff8ef4e03c1fee1f16346ed310e639ab211030472a1b284e1280`

```dockerfile
```

-	Layers:
	-	`sha256:42fad001fc654e00dd06916ae3ee7190c2b3df49ffc496849befc30dbe503fe0`  
		Last Modified: Thu, 15 Aug 2024 17:59:00 GMT  
		Size: 2.0 MB (2014524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eacfeb1ff9b1adb1601df78be43b0f78df517ef2ce13b2caf4dc25f3961da52`  
		Last Modified: Thu, 15 Aug 2024 17:59:00 GMT  
		Size: 12.9 KB (12926 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:150e68e5010f213f126b2b49ab53e494e9380a7ad7b333ebc6617c5159192868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.3 MB (106316770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b148197dc7886d4a9cf6275d447d375153bff51f1e0c07372a30b98cf408c5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 07:06:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Aug 2024 07:06:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_VERSION=8.0.8.30
# Thu, 15 Aug 2024 07:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='07df7f73c1ab08ca8adcfede1d35789fb36368d42226c32b998c36b84ace8aff';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='35bd6696ddb4a2ab54afc517efdd37ce3471cba589ebbcaad04019caec773510';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='32040e63bbf94b7a6e97ebcf28e4ba4c336c82b2e1c1131658e5762c82c204d7';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='11ee2b25766e7c4685f2f2a89f3bf54265a97c8ae52bcddd3a46a21e872ea436';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b823c911ee157eda0ab24a76ac49580a066062d8c3dbbe00bf159415ecbf49b6`  
		Last Modified: Thu, 15 Aug 2024 18:18:41 GMT  
		Size: 1.5 MB (1523275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda1176bf6d8a3cb8f19c13c46747333b9894209f5467ebd68e11bfacf8e01ae`  
		Last Modified: Thu, 15 Aug 2024 18:19:47 GMT  
		Size: 70.3 MB (70332414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:44e35f5b870aeb34c33c1e6fc5ac38425cc644f314e9f9b4c5cc27ed316dcfdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd869eca8e03b660b248da7c5bba9b87685dc9a795aa5244414fcd2d68e4939`

```dockerfile
```

-	Layers:
	-	`sha256:00448b3846a34c899b32e833037a04da01ab9784f21606b98e0444f9b57a8db6`  
		Last Modified: Thu, 15 Aug 2024 18:19:45 GMT  
		Size: 2.0 MB (2017765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8d3cdb0c2de1e662512671ec888f01ea1dbad4614e427f6d4ac9af12a76ce45`  
		Last Modified: Thu, 15 Aug 2024 18:19:44 GMT  
		Size: 13.0 KB (12955 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:d14c044fb946326a50064f8e2ee6fd7aff4050db523b695a1dddef23a9f7e144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.9 MB (99910587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c710be2324567b529140d6f72c75d73fbb244d3a6d6672264a800b6c8cc40d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Jun 2024 19:26:47 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:26:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:26:50 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Thu, 27 Jun 2024 19:26:50 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 07:06:00 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 15 Aug 2024 07:06:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_VERSION=8.0.8.30
# Thu, 15 Aug 2024 07:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='07df7f73c1ab08ca8adcfede1d35789fb36368d42226c32b998c36b84ace8aff';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='35bd6696ddb4a2ab54afc517efdd37ce3471cba589ebbcaad04019caec773510';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='32040e63bbf94b7a6e97ebcf28e4ba4c336c82b2e1c1131658e5762c82c204d7';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='11ee2b25766e7c4685f2f2a89f3bf54265a97c8ae52bcddd3a46a21e872ea436';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Thu, 15 Aug 2024 07:06:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:bc95fae2023d2ac4f35628ab3a262084bf2801462adfa6e7304b2b4e70ff4ab1`  
		Last Modified: Thu, 27 Jun 2024 20:18:52 GMT  
		Size: 28.0 MB (28000540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410f7d43033771545436ae5d16392e1bd692fce0abf07f6d40a2b30d83168ea5`  
		Last Modified: Thu, 15 Aug 2024 18:11:47 GMT  
		Size: 1.4 MB (1441950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b21ac64e844e09638f39f99d84fa8c4d4b4a6334464fa74040488ea374189d3`  
		Last Modified: Thu, 15 Aug 2024 18:12:46 GMT  
		Size: 70.5 MB (70468097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:c2d07d33097802ca0358290ed96925473540deb47f4cee422d46e81547cb6760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2029807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0a81596a1f74197d8268ba3676a639608de0f0e95430ae755bd60c828d8625`

```dockerfile
```

-	Layers:
	-	`sha256:a241966dd230b65e83c071d5356486be5b344274c568b149b924e419cd63e67c`  
		Last Modified: Thu, 15 Aug 2024 18:12:45 GMT  
		Size: 2.0 MB (2016880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ffa0ff8661a7d6f71928c419cbd804a4449f92ca614401c42a02b1d9984bcac`  
		Last Modified: Thu, 15 Aug 2024 18:12:45 GMT  
		Size: 12.9 KB (12927 bytes)  
		MIME: application/vnd.in-toto+json
