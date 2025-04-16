## `maven:3-sapmachine-24`

```console
$ docker pull maven@sha256:3ffe3ee53f059961cf9ff85ef21c7ba7aed4c5a8167d9cf1d38c14fc19a7fae0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-sapmachine-24` - linux; amd64

```console
$ docker pull maven@sha256:722787cddb8adaa2b8a520255842df3cd1af18a54669b83f163289faade0343f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.2 MB (299177285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30d5cae9fc75d273ce26c046e31e70337d6f39b0edc40ca01efc8f54244786b8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Mar 2025 16:03:48 GMT
ARG RELEASE
# Thu, 27 Mar 2025 16:03:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 27 Mar 2025 16:03:48 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["/bin/bash"]
# Thu, 27 Mar 2025 16:03:48 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["jshell"]
# Thu, 27 Mar 2025 16:03:48 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ARG MAVEN_VERSION=3.9.9
# Thu, 27 Mar 2025 16:03:48 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Mar 2025 16:03:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb74487086b0e317b63ed32b4dc0b06911fe4edb99d7db2daa58335d2f06ce69`  
		Last Modified: Wed, 16 Apr 2025 16:13:50 GMT  
		Size: 232.4 MB (232429425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194e9d512dfb7aa6728d49bae9256d7edce6708d833583da34050fad13a68f8b`  
		Last Modified: Wed, 16 Apr 2025 16:55:25 GMT  
		Size: 27.9 MB (27858723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088a74d6a4e43db32467cab64926a1792ee71d736ae4269b329e677a9f55ac89`  
		Last Modified: Wed, 16 Apr 2025 16:55:25 GMT  
		Size: 9.2 MB (9170446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43d8fdf132aab553356ab25f55abd1d83ba7784f4d1ee69ec2f9e590c53270d`  
		Last Modified: Wed, 16 Apr 2025 16:55:24 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1398a439ffdc9bbea81050a2c521132453ddbc78bd9f0c9f7f07c88b9accd69`  
		Last Modified: Wed, 16 Apr 2025 16:55:24 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-24` - unknown; unknown

```console
$ docker pull maven@sha256:850bc491179057f864425e34a3130f60d5e4613c59e4673c56fffc40e97d17e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4165113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9efc32dffb4e05a3906efe69b1c33a867327fdf75d3d4c8727d43458fcd8e6`

```dockerfile
```

-	Layers:
	-	`sha256:f398687a73616517ebdc10c5e2fb990d789d543526a5c654f46c2dce62c846d5`  
		Last Modified: Wed, 16 Apr 2025 16:55:24 GMT  
		Size: 4.1 MB (4148574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a26c9b1d0a2e88bf174e29bb0083caf8aee40e8931344f899c0dcf915d7bbab3`  
		Last Modified: Wed, 16 Apr 2025 16:55:24 GMT  
		Size: 16.5 KB (16539 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-24` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:f08d9fde81e77201267bb5991314f77923757c7ec12fe67b695dc4bd21423e1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.3 MB (296283921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c8fb5d09b77551c5f07099d11acad5e8f9c47636a4174a95fabd8a2e05ee7ff`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Mar 2025 16:03:48 GMT
ARG RELEASE
# Thu, 27 Mar 2025 16:03:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 27 Mar 2025 16:03:48 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["/bin/bash"]
# Thu, 27 Mar 2025 16:03:48 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["jshell"]
# Thu, 27 Mar 2025 16:03:48 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ARG MAVEN_VERSION=3.9.9
# Thu, 27 Mar 2025 16:03:48 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Mar 2025 16:03:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5b195d2485c8941fd3560db8bd21646133d98b318e6b2b3a280a57560e1e75`  
		Last Modified: Wed, 16 Apr 2025 16:13:51 GMT  
		Size: 230.4 MB (230360006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38536b11ecdf8a8066458c31f1a1f98c0f6431f3b8b1b9bf68c33473b928c5b0`  
		Last Modified: Wed, 16 Apr 2025 16:56:07 GMT  
		Size: 27.9 MB (27905483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d33476608eb7f71709983f78780a75d02f59f3f007bb2cdae530f953384234`  
		Last Modified: Wed, 16 Apr 2025 16:56:07 GMT  
		Size: 9.2 MB (9170433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60be5d5564282fe52a6c5d0c58e0e8f8250964aced59b34ec808516851a093c`  
		Last Modified: Wed, 16 Apr 2025 16:56:06 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a494f608ceb26f5b4dfd0913c3e202f5b53b8647facfcd3162e9d8a34174cb5`  
		Last Modified: Wed, 16 Apr 2025 16:56:07 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-24` - unknown; unknown

```console
$ docker pull maven@sha256:7134bf335593eaba1a9c158bf788815336fafaa6aa63a2eb6998329d77df747e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4171765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b030a39e83b3dfc9b09b70ecb6088be5d922f3a5fad020a58c52987f8d3b9c2d`

```dockerfile
```

-	Layers:
	-	`sha256:bb76bafb881c3554366252721b99c621585aea2e990e03774fdcadedecbbafab`  
		Last Modified: Wed, 16 Apr 2025 16:56:06 GMT  
		Size: 4.2 MB (4155093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ba4224bb1a9b2d3f27550df8072ea8222701c267ea7424ec824a73e7aa4c433`  
		Last Modified: Wed, 16 Apr 2025 16:56:06 GMT  
		Size: 16.7 KB (16672 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-24` - linux; ppc64le

```console
$ docker pull maven@sha256:f642a198b5fc5e5e15e507410c05455b7a80b54d3f33de1ba58abb782cc4d495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.8 MB (309832012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe3fae25f6e18aba3f8a2cbf0c86d79770110566d4570fa5c13078c57673f36`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Mar 2025 16:03:48 GMT
ARG RELEASE
# Thu, 27 Mar 2025 16:03:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 27 Mar 2025 16:03:48 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["/bin/bash"]
# Thu, 27 Mar 2025 16:03:48 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["jshell"]
# Thu, 27 Mar 2025 16:03:48 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ARG MAVEN_VERSION=3.9.9
# Thu, 27 Mar 2025 16:03:48 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Mar 2025 16:03:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1ad4ce3eb227a8a7956abe526af7257ad5fc3e8233c2195ab8136b6d33fb9e`  
		Last Modified: Wed, 16 Apr 2025 16:15:01 GMT  
		Size: 233.8 MB (233771063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b91dc3fc6e95dc3068c079930ff17956dbe023c3b7f5b2a3e87c9e0161ec494`  
		Last Modified: Wed, 16 Apr 2025 17:37:16 GMT  
		Size: 32.5 MB (32548609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ef7673f4acba0d36f4f575a7ae5c444d7e05503555daf309a2f79aaf21c2ae`  
		Last Modified: Wed, 16 Apr 2025 17:37:15 GMT  
		Size: 9.2 MB (9170434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64117e1f83cade22601cf3e4baed8f7dfb414d9dea880cf25a01ff5ab6b4757e`  
		Last Modified: Wed, 16 Apr 2025 17:37:17 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434a82cfaa1afb52c230c9783782b6f1d40040609411361f69702b759052bd8c`  
		Last Modified: Wed, 16 Apr 2025 17:37:15 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-24` - unknown; unknown

```console
$ docker pull maven@sha256:cdb4c2c0edf3784de87c6d40eac78643f1bf391732ff4ebb06b78533cfd220fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08bbc15c314218e44f7ce8027ad837346611c1f90ce23b2a0dab41baa129149d`

```dockerfile
```

-	Layers:
	-	`sha256:732b5190c9cd06582e622edcd27fe88a148dedc516080002bfcb97334c7c5e3a`  
		Last Modified: Wed, 16 Apr 2025 17:37:16 GMT  
		Size: 4.2 MB (4152810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04dc8d2608f125c7924dce0f9472bb1cbeb57ab69b54eec6bfda04b57a8403d1`  
		Last Modified: Wed, 16 Apr 2025 17:37:15 GMT  
		Size: 16.6 KB (16588 bytes)  
		MIME: application/vnd.in-toto+json
