## `maven:3-sapmachine-22`

```console
$ docker pull maven@sha256:43441c58faad83de435301e3e96e83b17a180521343f06e4ff715badcdbcbae3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-sapmachine-22` - linux; amd64

```console
$ docker pull maven@sha256:4cb93fde4853cd20394eec48c7662acf027f492f09cc31f15ed1050c4f9aad8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.9 MB (276876051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20268e9eb08a25ace5f755b63a6b50b139c748fcd3b27717aeff797fb9165e45`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
# Wed, 29 May 2024 20:51:55 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 20:51:55 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 29 May 2024 20:51:55 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 29 May 2024 20:51:55 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 29 May 2024 20:51:55 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 29 May 2024 20:51:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 29 May 2024 20:51:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 29 May 2024 20:51:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 29 May 2024 20:51:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 29 May 2024 20:51:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 29 May 2024 20:51:55 GMT
ARG MAVEN_VERSION=3.9.7
# Wed, 29 May 2024 20:51:55 GMT
ARG USER_HOME_DIR=/root
# Wed, 29 May 2024 20:51:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 29 May 2024 20:51:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 29 May 2024 20:51:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835f8f35c95610ca5687d9be749f7b06ba9d6bfd97fd5f43b56be3df494c0022`  
		Last Modified: Tue, 25 Jun 2024 22:57:48 GMT  
		Size: 213.8 MB (213790435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945c878003551d6e22d3afcdd4d389336865d9e8f4c43e6f2d90788163368c73`  
		Last Modified: Tue, 25 Jun 2024 23:57:20 GMT  
		Size: 23.7 MB (23731826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cca442c8cb0c1697d2c3135cc9a2e5786f2cea472cbb115999806c48f02bcb4`  
		Last Modified: Tue, 25 Jun 2024 23:57:20 GMT  
		Size: 9.6 MB (9647591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b38cb45fb19e3a1e5bfeae35459e218f42c195601a26244b3a599bbfa1ccb5`  
		Last Modified: Tue, 25 Jun 2024 23:57:19 GMT  
		Size: 858.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d103c6c98179bc3e3eb517892d681f77f60bca8d2b0160db00d1aa88c6440fbf`  
		Last Modified: Tue, 25 Jun 2024 23:57:19 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-22` - unknown; unknown

```console
$ docker pull maven@sha256:60513a434caa2dc0f4e6d074cc8353aee44d77af4850c3c29bca1e656b379fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4064627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9cacb56082cadec44fdc3be4cb11ed2aee38d092980dafc1a533f6854947d28`

```dockerfile
```

-	Layers:
	-	`sha256:df3748cff105b9ccae865c62d9a5cf732855f3475f303429a839a5daec141078`  
		Last Modified: Tue, 25 Jun 2024 23:57:19 GMT  
		Size: 4.0 MB (4048158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae8304176fd0bf291f296108d1021362c377174a7c2426d8ffffbc9d10f146dd`  
		Last Modified: Tue, 25 Jun 2024 23:57:19 GMT  
		Size: 16.5 KB (16469 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-22` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:3f4b1f64a9ef9482446224b910833461ad35481bebcc6b43b95e85c804e637b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.2 MB (275158002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc445b07429e198b13d32f8887ad4442e81a42ec98d1d8ffd2b138b85b6731b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 29 May 2024 20:51:55 GMT
ARG RELEASE
# Wed, 29 May 2024 20:51:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 29 May 2024 20:51:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 29 May 2024 20:51:55 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 29 May 2024 20:51:55 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Wed, 29 May 2024 20:51:55 GMT
CMD ["/bin/bash"]
# Wed, 29 May 2024 20:51:55 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Wed, 29 May 2024 20:51:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Wed, 29 May 2024 20:51:55 GMT
CMD ["jshell"]
# Wed, 29 May 2024 20:51:55 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 20:51:55 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 29 May 2024 20:51:55 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 29 May 2024 20:51:55 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 29 May 2024 20:51:55 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 29 May 2024 20:51:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 29 May 2024 20:51:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 29 May 2024 20:51:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 29 May 2024 20:51:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 29 May 2024 20:51:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 29 May 2024 20:51:55 GMT
ARG MAVEN_VERSION=3.9.7
# Wed, 29 May 2024 20:51:55 GMT
ARG USER_HOME_DIR=/root
# Wed, 29 May 2024 20:51:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 29 May 2024 20:51:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 29 May 2024 20:51:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5565bafaf15034498e7abe77b3a5c475e47a042ef7ec4c73b21a26c6ecd11d`  
		Last Modified: Mon, 17 Jun 2024 23:35:09 GMT  
		Size: 211.8 MB (211782120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74378643148fb8c7f93e9ed545e59f3bf9fa8555025d16e6be8197415ff3001`  
		Last Modified: Fri, 21 Jun 2024 17:06:10 GMT  
		Size: 23.8 MB (23819248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cec6c738272271f7b648c1e2476cf64997e255e420927db3f5f1d43ea83bef1`  
		Last Modified: Fri, 21 Jun 2024 17:06:10 GMT  
		Size: 9.6 MB (9647610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee376a17ff7f1c9350dfe946fb1d2ce67fca04652eb07b945385349c62585970`  
		Last Modified: Fri, 21 Jun 2024 17:06:10 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35da1ab85580c3ae097f8fdcc6d9033c6336c84e0afce5ba2ea672773768d6d6`  
		Last Modified: Fri, 21 Jun 2024 17:06:16 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-22` - unknown; unknown

```console
$ docker pull maven@sha256:bf23ca1e90867dbcd214eeee9ed03095846ac5e17b4718a8c9e159989fdf1229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4071017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc40a9efad6c8ddc29e240a942286fddc89e1ccf9e439ed9a7c4cb13abd7933f`

```dockerfile
```

-	Layers:
	-	`sha256:ec59d935231fed01b2ef0259725d7abcf5f78183e9616d11aac1fd991a8dc5bc`  
		Last Modified: Fri, 21 Jun 2024 17:06:10 GMT  
		Size: 4.1 MB (4054052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4a8902f8e9111c059ca33776470e17a0d2b2c49bd55b2b0c7b4643923047f45`  
		Last Modified: Fri, 21 Jun 2024 17:06:09 GMT  
		Size: 17.0 KB (16965 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-22` - linux; ppc64le

```console
$ docker pull maven@sha256:6d0bf7e5f3ec3aeb87a785ccbb1e95cd62edbe0a7d1eb1ae29d75fcb9f5ef629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.1 MB (288132666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280725c6829e1db557ddb2c35e348bb50fdf4a5aa294019f8d17fa9d9e59b2c1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 29 May 2024 20:51:55 GMT
ARG RELEASE
# Wed, 29 May 2024 20:51:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 29 May 2024 20:51:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 29 May 2024 20:51:55 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 29 May 2024 20:51:55 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Wed, 29 May 2024 20:51:55 GMT
CMD ["/bin/bash"]
# Wed, 29 May 2024 20:51:55 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Wed, 29 May 2024 20:51:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Wed, 29 May 2024 20:51:55 GMT
CMD ["jshell"]
# Wed, 29 May 2024 20:51:55 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 20:51:55 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 29 May 2024 20:51:55 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 29 May 2024 20:51:55 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 29 May 2024 20:51:55 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 29 May 2024 20:51:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 29 May 2024 20:51:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 29 May 2024 20:51:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 29 May 2024 20:51:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 29 May 2024 20:51:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 29 May 2024 20:51:55 GMT
ARG MAVEN_VERSION=3.9.7
# Wed, 29 May 2024 20:51:55 GMT
ARG USER_HOME_DIR=/root
# Wed, 29 May 2024 20:51:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 29 May 2024 20:51:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 29 May 2024 20:51:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a6b87acc0a568209f5593370b5b6bcffdf1ec82a13216fce26023e6eac0aaea8`  
		Last Modified: Sun, 09 Jun 2024 02:03:40 GMT  
		Size: 35.6 MB (35626958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cff25a4f62ff119b6b630b575cbcd5ba6077af919a30f57323bd4ecb27a8288`  
		Last Modified: Mon, 17 Jun 2024 23:08:22 GMT  
		Size: 215.0 MB (214997406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb21cce6b589433a1921cd6d43ad86334d7593e2e0144411ec0512221b5456a`  
		Last Modified: Fri, 21 Jun 2024 07:26:30 GMT  
		Size: 27.9 MB (27859658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8882ba40cbce19e05704aeba68b2a52294bcba6664f5e6fcb5201e6146928fb8`  
		Last Modified: Fri, 21 Jun 2024 07:26:29 GMT  
		Size: 9.6 MB (9647601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643e446594fdb0d1c65fb72f08346f744bd2756511ad6957eaa2e92edb449d03`  
		Last Modified: Fri, 21 Jun 2024 07:26:28 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a1b813b1f3e1d30b9881683ebd8c88a8aed56fc4a27705d5c3bed42ac8e453`  
		Last Modified: Fri, 21 Jun 2024 07:26:29 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-22` - unknown; unknown

```console
$ docker pull maven@sha256:424d61d71b5b2e7aef75ad1e8c0a92d5cb5bbc252e396c7dc355e7c952bfbcb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4068765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0acd9eedcf2efc608bc6eebb02e16c02dcac0fe13e5461f8690c6925d736cc99`

```dockerfile
```

-	Layers:
	-	`sha256:5123bf41d2cc3f0eead6f5c37b396b6866cfed6a029b5460f2721eb212723ebd`  
		Last Modified: Fri, 21 Jun 2024 07:26:28 GMT  
		Size: 4.1 MB (4052368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:792cca982efea0269084d8a66b8289420620f737b9fe73b5fa7330817035a2cc`  
		Last Modified: Fri, 21 Jun 2024 07:26:28 GMT  
		Size: 16.4 KB (16397 bytes)  
		MIME: application/vnd.in-toto+json
