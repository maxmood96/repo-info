## `maven:3-amazoncorretto-8-debian-bookworm`

```console
$ docker pull maven@sha256:acad860ecebfa74fdcc56094bb644a5456fee884753b2c4833b2b8448443424e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-debian-bookworm` - linux; amd64

```console
$ docker pull maven@sha256:2d50294f419f3bb104e13fa1a356ace3a5f134712142f9a0c74ad139c9ec438b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163704948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc845d7529ff1e55df36d976e7514e13844fd19b840c69ac72dadb0d2d23e810`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 07:27:41 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 16 Jul 2025 07:27:41 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '5fdaed0a262b975776b1d5c0170d2e86b1be1e98b27ef97114b04ec9ac7f011d *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Jul 2025 07:27:41 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 07:27:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Wed, 16 Jul 2025 07:27:41 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 07:27:41 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 07:27:41 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 07:27:41 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 07:27:41 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 07:27:41 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 07:27:41 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 07:27:41 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 07:27:41 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 07:27:41 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 07:27:41 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 07:27:41 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 07:27:41 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 07:27:41 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e92f64621aa8a32ae5e2543117685a61a58e61b6d220012889b53a4715b9c56`  
		Last Modified: Tue, 12 Aug 2025 21:37:11 GMT  
		Size: 126.2 MB (126231093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bab381865a0c7029999f09fd4cc7a608dbe420e77354bed18fb1446a7e42a69`  
		Last Modified: Tue, 12 Aug 2025 21:36:58 GMT  
		Size: 9.2 MB (9242567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9bc4e33e49be80ba1acd73c302f0e28b1b7edbb3258d68a8702bd9caf593d35`  
		Last Modified: Tue, 12 Aug 2025 21:36:57 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8088bf292ecac77b993d745f8120e3753d834c37c72e0b258279394c457e08`  
		Last Modified: Tue, 12 Aug 2025 21:36:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian-bookworm` - unknown; unknown

```console
$ docker pull maven@sha256:5dbee7673e00f2c6f50da8c5d4f3eacd924082eebfa73511a4bd1a9001c3284e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3028326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824294615e2bb724e5873dcfea244f0f57758a5bf3745a26b6aec06f0b8aeb1d`

```dockerfile
```

-	Layers:
	-	`sha256:1d0fe6b9d150b117cf2c79fed0f92e53e55462d3435cb7ec97f2dbca4b035eab`  
		Last Modified: Tue, 12 Aug 2025 23:27:50 GMT  
		Size: 3.0 MB (3009053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9822ceb8a0b1d21efe2a9650a6ce0ada14ba69086b8f5d90545af2f2bf8637d`  
		Last Modified: Tue, 12 Aug 2025 23:27:51 GMT  
		Size: 19.3 KB (19273 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-debian-bookworm` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:c4a690cf6478a874dd5319cd14de651953c5f53489386ef929aff0eb7d39343a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.3 MB (147340071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da2b4b971ced84d8c734c0e01c51a462c5998a1e21f33ddb2cb2cd449957f13c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 07:27:41 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 16 Jul 2025 07:27:41 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '5fdaed0a262b975776b1d5c0170d2e86b1be1e98b27ef97114b04ec9ac7f011d *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Jul 2025 07:27:41 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 07:27:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Wed, 16 Jul 2025 07:27:41 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 07:27:41 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 07:27:41 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 07:27:41 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 07:27:41 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 07:27:41 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 07:27:41 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 07:27:41 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 07:27:41 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 07:27:41 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 07:27:41 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 07:27:41 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 07:27:41 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 07:27:41 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13d7500edeea44a100b9b2e056fef33650921ed1c44ae2a6d7935a505a58310`  
		Last Modified: Wed, 13 Aug 2025 20:09:58 GMT  
		Size: 110.0 MB (110014448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef94a1931a4b9bfbc50a57635826f9147bebff7320b97df2ff2678c80ad6eb5`  
		Last Modified: Wed, 13 Aug 2025 20:09:31 GMT  
		Size: 9.2 MB (9242585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5899ab144dd6aea3212dd1fb329bca2c8a1c525ce482a4a72368b3b530e4800`  
		Last Modified: Wed, 13 Aug 2025 20:09:30 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e7caf00c4714383de01a1f2c8e225e4c65fe1adaf99d28fb7adb3a65defd25`  
		Last Modified: Wed, 13 Aug 2025 20:09:30 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian-bookworm` - unknown; unknown

```console
$ docker pull maven@sha256:e53d8c0257ba0aebe4a55a87e751e9b10cafca70772a5244016f0949f1880eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3011313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20c3acfeb2c58b6a87dd352753313382b97e947826ae64c35c5958d5ba429ae5`

```dockerfile
```

-	Layers:
	-	`sha256:d1dfed127813ff7563e9eb1d13127780afc7b42060bb1e508acdfd818b992132`  
		Last Modified: Wed, 13 Aug 2025 20:28:38 GMT  
		Size: 3.0 MB (2991871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bf82ab33c4cb57746975089a71e59585c8ac06b5ac4f329212c9d30019ffc00`  
		Last Modified: Wed, 13 Aug 2025 20:28:39 GMT  
		Size: 19.4 KB (19442 bytes)  
		MIME: application/vnd.in-toto+json
