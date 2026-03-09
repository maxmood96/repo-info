## `maven:sapmachine`

```console
$ docker pull maven@sha256:b0d73af5c24959ab1d73e8c7ce86010fb326b1bc2c10000b7d05c9b66eacb2a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:sapmachine` - linux; amd64

```console
$ docker pull maven@sha256:9839eed3c76969635ce9caef41ea53a1af3e9a125aac2d006ed4f2b6e5d484ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286346596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:163ebf8bbc8b7db6662b1655e5ad8c61a6cda0a2b80e57d8d244068157de4f6f`
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
# Tue, 17 Feb 2026 20:32:14 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:32:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Feb 2026 20:32:14 GMT
CMD ["jshell"]
# Mon, 09 Mar 2026 19:15:21 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Mar 2026 19:15:22 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 09 Mar 2026 19:15:22 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:15:22 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:15:22 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 09 Mar 2026 19:15:22 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 09 Mar 2026 19:15:22 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 09 Mar 2026 19:15:22 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 09 Mar 2026 19:15:22 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 09 Mar 2026 19:15:22 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 09 Mar 2026 19:15:22 GMT
ARG MAVEN_VERSION=3.9.13
# Mon, 09 Mar 2026 19:15:22 GMT
ARG USER_HOME_DIR=/root
# Mon, 09 Mar 2026 19:15:22 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 09 Mar 2026 19:15:22 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 09 Mar 2026 19:15:22 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59dd241bd37e489d34f787cd165d1a11f24b0c28a00cfa30c44e70c91094c547`  
		Last Modified: Tue, 17 Feb 2026 20:32:38 GMT  
		Size: 221.5 MB (221452841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0d9b8abb924d64ed59ce231d37e6aaccb42a1e35125d14acec2f2a3cf5dcaa`  
		Last Modified: Mon, 09 Mar 2026 19:15:35 GMT  
		Size: 25.5 MB (25467594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0310e98150a4929bdb348470e270a3406167f087b13b2e7c4406739fda30c6bb`  
		Last Modified: Mon, 09 Mar 2026 19:15:34 GMT  
		Size: 9.7 MB (9697513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:732bc96b6602e612b53a0db3c2eba508cd158675f4de4a41731d8696111e0c3d`  
		Last Modified: Mon, 09 Mar 2026 19:15:34 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b31f80cfa32c74c13f4c388bc67fdb85937f170424aaeb93e4890713d27cc8a`  
		Last Modified: Mon, 09 Mar 2026 19:15:34 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:63d54e716385f5f7428a2e812a3925dfdd9725720d78b26a59824f94c3da6422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4337282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472c9a4f4972b69f78f9e0148415663c578cbadeff58c51b4ecffaed8f5b0378`

```dockerfile
```

-	Layers:
	-	`sha256:8941cb347ad8cf15e5637a65922c0b162e619a1b3a03b7ca6a6b7a6278787b9d`  
		Last Modified: Mon, 09 Mar 2026 19:15:34 GMT  
		Size: 4.3 MB (4319537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f22f6eba2bb611c850b52317545fcc67da7cdb740abaecc3aa6fe98b80c40c68`  
		Last Modified: Mon, 09 Mar 2026 19:15:34 GMT  
		Size: 17.7 KB (17745 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:sapmachine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:17da178b09363f44d3e0e875147ba92864d1c801e0082ecd9c9ddf6f7e57c5a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 MB (283362681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6104890bdb42806a52cef37f1ad11f0c4e82421a7634929190e8762358e9ace8`
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
# Tue, 17 Feb 2026 20:31:21 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:31:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Feb 2026 20:31:21 GMT
CMD ["jshell"]
# Mon, 09 Mar 2026 19:15:09 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Mar 2026 19:15:09 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 09 Mar 2026 19:15:09 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:15:09 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:15:09 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 09 Mar 2026 19:15:09 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 09 Mar 2026 19:15:09 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 09 Mar 2026 19:15:09 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 09 Mar 2026 19:15:09 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 09 Mar 2026 19:15:09 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 09 Mar 2026 19:15:09 GMT
ARG MAVEN_VERSION=3.9.13
# Mon, 09 Mar 2026 19:15:09 GMT
ARG USER_HOME_DIR=/root
# Mon, 09 Mar 2026 19:15:09 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 09 Mar 2026 19:15:09 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 09 Mar 2026 19:15:09 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63210ec8e29a90dd08e5d25f72bdeb405e7aa2e604119720f6cb0ee9275c1387`  
		Last Modified: Tue, 17 Feb 2026 20:31:45 GMT  
		Size: 219.3 MB (219265992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d794a3a92828069a3322a8c99b7e66baae43165b7e8b033330818f8f8fd69e61`  
		Last Modified: Mon, 09 Mar 2026 19:15:23 GMT  
		Size: 25.5 MB (25532989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433d9b54af7fc50663991028ca785867402bb07f91f9dbf88b1dffa69527687a`  
		Last Modified: Mon, 09 Mar 2026 19:15:22 GMT  
		Size: 9.7 MB (9697544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c59150bbf3413dd85520a3fd41ea894c6cd1995014bcb7ef1897f0a8706e6c1`  
		Last Modified: Mon, 09 Mar 2026 19:15:22 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4121a87e6aaaff59186a0cc0777369410d398b5992a3333e1d3cce3d05aba4c`  
		Last Modified: Mon, 09 Mar 2026 19:15:22 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:6abf973d222c6fc197c90fefe9ca9c84f028f7a4a4e11795c789e9c9884e7754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4344029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb97bee967fe33d43b6149317285f7ec047154474a176ece60aa1bed2e810de4`

```dockerfile
```

-	Layers:
	-	`sha256:e3c37a03c51287d48e15aa51e67a80e859e1681d97765f0836c13c426d02a0f0`  
		Last Modified: Mon, 09 Mar 2026 19:15:22 GMT  
		Size: 4.3 MB (4326104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5259c7b0d99412d9c6effea6b1787369075414f4b52f7d10a49edcce5a28fa8b`  
		Last Modified: Mon, 09 Mar 2026 19:15:22 GMT  
		Size: 17.9 KB (17925 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:sapmachine` - linux; ppc64le

```console
$ docker pull maven@sha256:1930fa79db3090c7d435ba2c104a8f14b9497d8ff7743bde3711b3986ba1e4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296381110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:193817f08ccf255139651ef1500885cc7e7cd5a0b002e786b729f4a628c8924c`
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
# Tue, 17 Feb 2026 21:15:12 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:15:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Feb 2026 21:15:12 GMT
CMD ["jshell"]
# Mon, 09 Mar 2026 21:23:34 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Mar 2026 21:23:35 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 09 Mar 2026 21:23:35 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 21:23:35 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 21:23:35 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 09 Mar 2026 21:23:35 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 09 Mar 2026 21:23:35 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 09 Mar 2026 21:23:35 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 09 Mar 2026 21:23:35 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 09 Mar 2026 21:23:36 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 09 Mar 2026 21:23:36 GMT
ARG MAVEN_VERSION=3.9.13
# Mon, 09 Mar 2026 21:23:36 GMT
ARG USER_HOME_DIR=/root
# Mon, 09 Mar 2026 21:23:36 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 09 Mar 2026 21:23:36 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 09 Mar 2026 21:23:36 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ffd89d86dbd458a58533c359a539d854ce70cdc772c7d9f919cfaf14f31435`  
		Last Modified: Tue, 17 Feb 2026 21:16:03 GMT  
		Size: 222.4 MB (222382623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647fa706daa13b9fe27d687cc953cdeb6559d5a414dab24a86bfd1513d36c625`  
		Last Modified: Mon, 09 Mar 2026 21:24:04 GMT  
		Size: 30.0 MB (29992997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1296985d111df05bb877a89ba4ccd352b7e37eafed6e867a1db03052976666b8`  
		Last Modified: Mon, 09 Mar 2026 21:24:04 GMT  
		Size: 9.7 MB (9697544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8093dfab9eb87e882a090d6443f7bd3c58312ebef76d5508d7c77e83998e8bf`  
		Last Modified: Mon, 09 Mar 2026 21:24:03 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b83b6f657a20bcb930ba4daac061a0b00dca4fa2d2b8a5c4d878f25ea5ea54`  
		Last Modified: Mon, 09 Mar 2026 21:24:03 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:e8305f84ea2bdbc2fd8e52f7650f9ea0b407fcb2752a7fb57b7767b037d96b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4337191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac60c49fb117ce88f5b3c8e5d87e49f3a5a683f98f08ad157b5a84dda7004d79`

```dockerfile
```

-	Layers:
	-	`sha256:a54ae44c9a8cd9fb4c2496ee4085c4a6deb6b0c16a06af0f9489ce036befbb1a`  
		Last Modified: Mon, 09 Mar 2026 21:24:03 GMT  
		Size: 4.3 MB (4319372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42d9de946d69b09d139ae0dafc72dd40ba482287e70c4a724a15f4cf5fb0c67a`  
		Last Modified: Mon, 09 Mar 2026 21:24:03 GMT  
		Size: 17.8 KB (17819 bytes)  
		MIME: application/vnd.in-toto+json
