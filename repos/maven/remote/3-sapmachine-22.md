## `maven:3-sapmachine-22`

```console
$ docker pull maven@sha256:8c9253635ed091baf6f89ec74d1249943865e9577249510e7d4b3fd084d53b48
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
$ docker pull maven@sha256:2104a881187ca2d9696d08ce8ace593edd0382bc8049b889b5109f77978dfea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.2 MB (276220802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18187918142210c668955357f46ca600cc8ee7ff3c959b9e82ae2731b0c2e8a4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
ARG RELEASE
# Thu, 27 Jun 2024 09:17:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 27 Jun 2024 09:17:07 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["jshell"]
# Thu, 27 Jun 2024 09:17:07 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:31e907dcc94a592a57796786399eb004dcbba714389fa615f5efa05a91316356`  
		Last Modified: Thu, 01 Aug 2024 15:42:11 GMT  
		Size: 29.7 MB (29706298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ca8ce58b3c78ea16efea1d2c0fcf4243a9387951162e4d90a124ff10d9b29d`  
		Last Modified: Sat, 17 Aug 2024 02:05:42 GMT  
		Size: 213.6 MB (213619262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab310848e338f43ddf2019ae39d4b2504a5cd5161312169316bb842aa6ebb23`  
		Last Modified: Sat, 17 Aug 2024 04:07:43 GMT  
		Size: 23.7 MB (23732390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3547e0c33004faae6960b1d360fdefac7e238879c8e70cf920c6602c952af1a4`  
		Last Modified: Sat, 17 Aug 2024 04:07:43 GMT  
		Size: 9.2 MB (9161815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c02c825021632b381889470cb258c3ade265792d501d09229f18ad01055151`  
		Last Modified: Sat, 17 Aug 2024 04:07:43 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e124c03bf687a16875846abcc960dfd760a77d45bc4d5875b25b30a6565f70`  
		Last Modified: Sat, 17 Aug 2024 04:07:43 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-22` - unknown; unknown

```console
$ docker pull maven@sha256:45c6b1198af3943a03e3a3be787b8957eca36391015a70c73e9eb3260c036f35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4104123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8552f59a8efa1e1a0f522886f6fee93916b31ebe515734452dfed66c957c305`

```dockerfile
```

-	Layers:
	-	`sha256:0004a935350540e0b21a857d58b67927e38316c01552911683690d97d2ec6afb`  
		Last Modified: Sat, 17 Aug 2024 04:07:43 GMT  
		Size: 4.1 MB (4087653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b57655e16431caa1c009225ae819b26ff2e2ed0bd7384668d48b3815f8fd819`  
		Last Modified: Sat, 17 Aug 2024 04:07:43 GMT  
		Size: 16.5 KB (16470 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-22` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:ccacf96a35c13dc788658473e1d2e89a02f71a9c175c4dae184533226df9a2dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.4 MB (273436077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213943ad908a6da24dd8b2427d6593e9ebef0508985858535c64a9ffc95f6fb1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["jshell"]
# Thu, 27 Jun 2024 09:17:07 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71aa85ab9ff65f99e92b615b0628854e41629b4c7a15c83606c19dc40a2d8e3b`  
		Last Modified: Fri, 19 Jul 2024 23:56:14 GMT  
		Size: 211.6 MB (211610955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c08ef7cba0b8a8ae3982203c0366e4ef1c8c7e57826fd93371ebe052af5e538`  
		Last Modified: Wed, 24 Jul 2024 19:19:47 GMT  
		Size: 23.8 MB (23819258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11766bdc2661419e14f341e67d0f71e88bdc9e0f25ba2b32edc4e48a320f92b`  
		Last Modified: Wed, 24 Jul 2024 19:19:47 GMT  
		Size: 9.2 MB (9161783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b25e63fdf10efb69d0e5f8a9771712159edffdd56e7f3f86dd50df8489ba73`  
		Last Modified: Wed, 24 Jul 2024 19:19:46 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0c2be97a4db0867f478717f31a99e222f488ee8e3827753c2dea1b919d6a65`  
		Last Modified: Wed, 24 Jul 2024 19:19:47 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-22` - unknown; unknown

```console
$ docker pull maven@sha256:2de3cff43f62cb65addc8f7597f4420d7578b8340255ba423295ea0225e1e878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4110721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec32b3f23b3261226367faf9581da9807222324aa9dee647c3aeafd4e5ae62e7`

```dockerfile
```

-	Layers:
	-	`sha256:22697f8d322a3cd0b6ae679ce564319f35a196c63546d8c60bb74feb5951ab7e`  
		Last Modified: Fri, 26 Jul 2024 02:19:34 GMT  
		Size: 4.1 MB (4093527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa22b6fd2774c1876d4e971dc1e6d74d8372f43ebf85b6d5626647e8f1ac16c0`  
		Last Modified: Fri, 26 Jul 2024 02:19:34 GMT  
		Size: 17.2 KB (17194 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-22` - linux; ppc64le

```console
$ docker pull maven@sha256:e13b6e2af6f620a261da76c149f2de04436b7f6cb1e668bcbbe19ae8655f0ec0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.4 MB (286369871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6490a862de6bb267c20b759263a1691fe3b906fc87769a39b8e1504cbd1440c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
ARG RELEASE
# Thu, 27 Jun 2024 09:17:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 27 Jun 2024 09:17:07 GMT
ADD file:f6dda5643c6c5671bba452213beef0fdd84c17bc5e733964b8b6d98a44d522a3 in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["jshell"]
# Thu, 27 Jun 2024 09:17:07 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:4f16ff2741334b0be5d9f311961a37c8bd0feb2974974ec52a327bbae3866e29`  
		Last Modified: Thu, 01 Aug 2024 15:42:28 GMT  
		Size: 34.5 MB (34507572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9532c4c5000556df154a237634817f3c1c27c39c6d8ec47c69390d07b795c34f`  
		Last Modified: Sat, 17 Aug 2024 02:25:41 GMT  
		Size: 214.8 MB (214838877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a057beb8662773466a8f7d2cae5abe2b717d091c4f3ad52b9e3f3d33145ea5b`  
		Last Modified: Sat, 17 Aug 2024 11:57:13 GMT  
		Size: 27.9 MB (27860569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a13cdae8f16a1584bd2ee03af3b6c4d1a69fc7a88e2ab36b8755fa67d4a4b9c`  
		Last Modified: Sat, 17 Aug 2024 11:57:13 GMT  
		Size: 9.2 MB (9161814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9681af58dd0893cbd4092328866fc871001a88f95759a8a42fb9fe53ca3f276`  
		Last Modified: Sat, 17 Aug 2024 11:57:13 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c85a22b2da402c2a576ed66e3c7116b2bd39d6001a6ec36156e9dfc0a31237`  
		Last Modified: Sat, 17 Aug 2024 11:57:12 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-22` - unknown; unknown

```console
$ docker pull maven@sha256:eb88ec061106e1f4e59e1e7039f89e77238ef716aa8caa11d4817d329c4f6d5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4108413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b40cf7b2dc6acfd7be9a95b511fed2623c16ff09e05bd6435aa601b098499fbf`

```dockerfile
```

-	Layers:
	-	`sha256:ffbd2f3e917277a7142db5ec67b30cc82b60e8ade225e500c9c9a6d826ccf797`  
		Last Modified: Sat, 17 Aug 2024 11:57:13 GMT  
		Size: 4.1 MB (4091863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95bf7223a77156b2d9aff1f8ba9029fc1c7100ae5734e39b6a0907efd7b40271`  
		Last Modified: Sat, 17 Aug 2024 11:57:12 GMT  
		Size: 16.6 KB (16550 bytes)  
		MIME: application/vnd.in-toto+json
