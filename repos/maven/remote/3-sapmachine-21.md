## `maven:3-sapmachine-21`

```console
$ docker pull maven@sha256:9222f968177190d769ce78fc28c764d4e54c19ed31224cf0a25ca532c4460b7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-sapmachine-21` - linux; amd64

```console
$ docker pull maven@sha256:d9109bf8fe224178ec1cda349d82059ccddc5d8bc92fc03123191a1a4895c5e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.9 MB (280888766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7789e85bb4891f4255b72a9c6534577c0ec27495748e74692c6be88a376ce84`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:34:28 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.10 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:34:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Feb 2026 20:34:28 GMT
CMD ["jshell"]
# Tue, 17 Feb 2026 22:30:54 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 22:30:54 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Feb 2026 22:30:54 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:30:54 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:30:54 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Feb 2026 22:30:54 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Feb 2026 22:30:54 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Feb 2026 22:30:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 22:30:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Feb 2026 22:30:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Feb 2026 22:30:55 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 17 Feb 2026 22:30:55 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Feb 2026 22:30:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Feb 2026 22:30:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Feb 2026 22:30:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8274a838a564442bb86c42115b06298c812b9ab3ebb06b5fb95e830bf3216a`  
		Last Modified: Tue, 17 Feb 2026 20:34:57 GMT  
		Size: 216.4 MB (216383437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a637bd6a93d3a53887c6dcc6fac9e40ced1bb71a87453a1d2c7af0fab01a2bf`  
		Last Modified: Tue, 17 Feb 2026 22:31:10 GMT  
		Size: 25.5 MB (25464433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeaac2b14da23423e29d902471ccaaaddd062217d4b3e06ddcbec5bd246933c5`  
		Last Modified: Tue, 17 Feb 2026 22:31:10 GMT  
		Size: 9.3 MB (9312251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a661bb2e4b5b2dc8d8ee72e52a50c80af41faed4d0e4f64f8aaf03aa1923945c`  
		Last Modified: Tue, 17 Feb 2026 22:31:09 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28648359f3c177fb4ca9ee9b9c4ddd608c7e06cbc9df1b237d8a0f4b8457614`  
		Last Modified: Tue, 17 Feb 2026 22:31:09 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-21` - unknown; unknown

```console
$ docker pull maven@sha256:0a44a81c3318c61f1df446636e1b8131ca4a41ae38e72b1127ad9abc1bab6208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4338871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74892e1158f47a96db347ba1275c526f584702e52665a0148ac87fe26005090a`

```dockerfile
```

-	Layers:
	-	`sha256:b9f116ae7244f65c9a0f186aee89623e1cf4b5d2f3312019ffeb9fe8ff737461`  
		Last Modified: Tue, 17 Feb 2026 22:31:09 GMT  
		Size: 4.3 MB (4322368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:843cbdb67c7631689090fd1144978fe17ed3038504b46f53b7cebdbd0a85bac8`  
		Last Modified: Tue, 17 Feb 2026 22:31:09 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:2278a9c50d7a48805ab74e0130a7bfc54586156a368f7a95a476f7b8be954fa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.4 MB (278352188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70fb54791ed20e02ba3210a6525c853ced32532c49fe3c011c9d1a7421dbd9e6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:33:19 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.10 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:33:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Feb 2026 20:33:19 GMT
CMD ["jshell"]
# Tue, 17 Feb 2026 22:19:38 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 22:19:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Feb 2026 22:19:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:19:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:19:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Feb 2026 22:19:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Feb 2026 22:19:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Feb 2026 22:19:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 22:19:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Feb 2026 22:19:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Feb 2026 22:19:38 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 17 Feb 2026 22:19:38 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Feb 2026 22:19:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Feb 2026 22:19:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Feb 2026 22:19:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd231f438b395d80c74bf75e355be29a389370ab936bc4cb0b20ee1e97eb99dd`  
		Last Modified: Tue, 17 Feb 2026 20:33:48 GMT  
		Size: 214.6 MB (214641498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa8f4896836b9d9d959ee1f3b83b7dcefe8e6fb193e9e58d09a52424dbe246b`  
		Last Modified: Tue, 17 Feb 2026 22:19:54 GMT  
		Size: 25.5 MB (25532277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d1e569acbdd1a152f2a2f33f9e820e2bca726c35c337665a945af14ef096b6`  
		Last Modified: Tue, 17 Feb 2026 22:19:53 GMT  
		Size: 9.3 MB (9312256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92cf10f98457d2f9fddedb133c1b9e91472e1fece7856be5b23386620ac9f883`  
		Last Modified: Tue, 17 Feb 2026 22:19:52 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430c6453d3f8ee262e1a3910e64e5704cd08bb95eace8926707ac810bcf38df2`  
		Last Modified: Tue, 17 Feb 2026 22:19:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-21` - unknown; unknown

```console
$ docker pull maven@sha256:c2a1131034057a06f9b53136b783e1309acc961909b30af70232d7179e4e3d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4345526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea5ad7ff9265b4dd9f0b0e1737bfd7b1386301d1a55e3dbb93f44bba40f29b5`

```dockerfile
```

-	Layers:
	-	`sha256:7601568f541b6b81b7cd86810d094b9d8b048d6a15299fecc787e6a17ae4cd19`  
		Last Modified: Tue, 17 Feb 2026 22:19:52 GMT  
		Size: 4.3 MB (4328890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:436121aa69c238b3e98d86a5d4f229a3b3654b495644fe8cc827a9cb3c9c740f`  
		Last Modified: Tue, 17 Feb 2026 22:19:52 GMT  
		Size: 16.6 KB (16636 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-21` - linux; ppc64le

```console
$ docker pull maven@sha256:550704f1ef9c80f28d0436d745f90efa5a7fa7b8a9f2f763d7c49bec48dbda46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291035193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b118b78259c5ecdb515b14f7a65d1399ad01257328d52135713d95ded1d546`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 21:25:31 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.10 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:25:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Feb 2026 21:25:31 GMT
CMD ["jshell"]
# Wed, 18 Feb 2026 02:48:09 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Feb 2026 02:48:10 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 18 Feb 2026 02:48:10 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 18 Feb 2026 02:48:10 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 18 Feb 2026 02:48:10 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 18 Feb 2026 02:48:10 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 18 Feb 2026 02:48:10 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 18 Feb 2026 02:48:10 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 18 Feb 2026 02:48:11 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 18 Feb 2026 02:48:12 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 18 Feb 2026 02:48:12 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 18 Feb 2026 02:48:12 GMT
ARG USER_HOME_DIR=/root
# Wed, 18 Feb 2026 02:48:12 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 18 Feb 2026 02:48:12 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 18 Feb 2026 02:48:12 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3dddb1b79b988fd01656ebf9c98d15b9f8cedfe95a50710f0549e121d4daf3`  
		Last Modified: Tue, 17 Feb 2026 21:26:17 GMT  
		Size: 217.4 MB (217425453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5443bfaa3f2b7b2bf8b430f73c942294358063ab360b5004fecff1ad1f3dcf1d`  
		Last Modified: Wed, 18 Feb 2026 02:49:05 GMT  
		Size: 30.0 MB (29989556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc5f01f3432d37cb509a91a652321144dc7300251ecd432fa92eac632d51f2d`  
		Last Modified: Wed, 18 Feb 2026 02:48:59 GMT  
		Size: 9.3 MB (9312242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fb187413a08530db474a69c108c8780028103fce2ef29e7a8afa5ea6b57bd3`  
		Last Modified: Wed, 18 Feb 2026 02:48:59 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85389943fc085f345b1e38bce4b2ebb809df01356a5663729eeeff4b81bfa4c1`  
		Last Modified: Wed, 18 Feb 2026 02:48:58 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-21` - unknown; unknown

```console
$ docker pull maven@sha256:6f7535d5caa39d365fde0cf226717f3b5b6816ee7398094061089bccf0f7a532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4339350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371eea1ffec1471558c347161a6dbc9fa077924647479ee818af61d47bda6737`

```dockerfile
```

-	Layers:
	-	`sha256:3e49ee9a8bca0b409d854b13641e93ff0b6e90ba047ea5af10ba5b782719bd08`  
		Last Modified: Wed, 18 Feb 2026 02:48:59 GMT  
		Size: 4.3 MB (4322797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d74b63c18bbb5f18f76998f3516e3732d38c04bb81a8c75d4fd4c649b8566c90`  
		Last Modified: Wed, 18 Feb 2026 02:48:58 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json
