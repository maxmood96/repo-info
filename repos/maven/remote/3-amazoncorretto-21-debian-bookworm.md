## `maven:3-amazoncorretto-21-debian-bookworm`

```console
$ docker pull maven@sha256:6937094365207173b9e5b02834453586d1508dd43f28258498f79462ff5ecd4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-debian-bookworm` - linux; amd64

```console
$ docker pull maven@sha256:aa3caffc56902b807d4ce879583edaf3681ddbe110d8bd8b3f910a057b576a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256214401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84b4e41887446c219e8cc62bd953ca1116907882d5891f7668d40915363ee69`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 19 Aug 2024 08:57:28 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["bash"]
# Mon, 19 Aug 2024 08:57:28 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 19 Aug 2024 08:57:28 GMT
ARG USER_HOME_DIR=/root
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ed2f323754e202de8cc5e414229b6387f72a76b2fcb024bd5f1f235e4b9544`  
		Last Modified: Wed, 04 Sep 2024 23:12:52 GMT  
		Size: 217.9 MB (217916437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df34d5e133817e985202f671b72bbe82e43da0db3d1f235d7f9c103c73a9160`  
		Last Modified: Wed, 04 Sep 2024 23:12:49 GMT  
		Size: 9.2 MB (9170441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2c82946ff7b0ccde59d75809669dbf6c8d80920bd45ff22362fe280db06e95`  
		Last Modified: Wed, 04 Sep 2024 23:12:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6301f2036ad933d0de94fe14effcf9b8b9f14cea8f05893c35b18cc05a64e777`  
		Last Modified: Wed, 04 Sep 2024 23:12:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-debian-bookworm` - unknown; unknown

```console
$ docker pull maven@sha256:d23d8daa8e8f647232c0cf3ad4bcdb5f2001913bbc98d100da88ed5575af183e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2999527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb2fbe3593fe9475b6f2d754497c48cf9902b0a090cbadab75b5775f825fd57`

```dockerfile
```

-	Layers:
	-	`sha256:3b087631a0a9438a6a49ed6753d0bd2637331f53e9fd2c5ac22f5a0e377f8bcf`  
		Last Modified: Wed, 04 Sep 2024 23:12:49 GMT  
		Size: 3.0 MB (2981039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:697e90f0b6ddbd7e4a468a0a1ddbd8193ee516988d00ab707841f4e1ba7a4d7c`  
		Last Modified: Wed, 04 Sep 2024 23:12:49 GMT  
		Size: 18.5 KB (18488 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-debian-bookworm` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:3740ec1dcfde1144a0442458bc0a3f68e8692f8b38924df6f837208019102e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 MB (253959416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68c228be76be1a7d07287464dab132ebbdefc815c48679d7300314c930adb7a0`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 19 Aug 2024 08:57:28 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["bash"]
# Mon, 19 Aug 2024 08:57:28 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key | gpg --batch --import   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 19 Aug 2024 08:57:28 GMT
ARG USER_HOME_DIR=/root
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f857385ec942400a555d7865db2156e9937aa74901a31c96ea73b805b302b0`  
		Last Modified: Thu, 05 Sep 2024 20:54:47 GMT  
		Size: 215.6 MB (215631394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c161d0c5c85627a5e021bd9c20480b6c64c34600944a1c473cbc2143705fd4c0`  
		Last Modified: Thu, 05 Sep 2024 20:54:42 GMT  
		Size: 9.2 MB (9170440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3073fa5eb15e99b43b7b31d77a975d3898eacd4a63d74b296ca485e2034c6dee`  
		Last Modified: Thu, 05 Sep 2024 20:54:42 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b8f4e855de43f859b7d061137236a82dfaf692d21f4aa02b2a91a6d6c65e6f`  
		Last Modified: Thu, 05 Sep 2024 20:54:42 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-debian-bookworm` - unknown; unknown

```console
$ docker pull maven@sha256:1df0f99948d1dd4becf110bdd965798f4d95f77b1fa437d11f5ae3a89f0f3c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2999870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170e2670a542c9f3bb4cdd27ddbe887be1153bc2ab2a19a269d3118a1f3f9f86`

```dockerfile
```

-	Layers:
	-	`sha256:94cba0bbd16a87b8714ae7276aaa9e114bb339d181da79888d34b4fecd75b976`  
		Last Modified: Thu, 05 Sep 2024 20:54:42 GMT  
		Size: 3.0 MB (2980697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:421127bfb16480bd6a78eff4952377ac6af9f4c0eb3e02d8811735c0b7492e0b`  
		Last Modified: Thu, 05 Sep 2024 20:54:42 GMT  
		Size: 19.2 KB (19173 bytes)  
		MIME: application/vnd.in-toto+json
