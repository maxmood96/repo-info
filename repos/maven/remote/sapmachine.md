## `maven:sapmachine`

```console
$ docker pull maven@sha256:df81aff73d522a1f672e44f6c8da3aa9daa1e2eda870ea89b6261411a106d395
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
$ docker pull maven@sha256:7518e943590e539485ac0e483175ed552cc86311d5ad4c8d05778cd73c3827a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.9 MB (284929884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50acae5fc2ed44d47e577d715e3e95758c2e3017d5b0f371c56a03bac1122be8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:37:25 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 13 Nov 2025 23:37:25 GMT
CMD ["jshell"]
# Wed, 17 Dec 2025 20:07:16 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 20:07:17 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 17 Dec 2025 20:07:17 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:07:17 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:07:17 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 17 Dec 2025 20:07:17 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 17 Dec 2025 20:07:17 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 17 Dec 2025 20:07:17 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 17 Dec 2025 20:07:17 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 17 Dec 2025 20:07:17 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 17 Dec 2025 20:07:17 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 17 Dec 2025 20:07:17 GMT
ARG USER_HOME_DIR=/root
# Wed, 17 Dec 2025 20:07:17 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 17 Dec 2025 20:07:17 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 17 Dec 2025 20:07:17 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb65f3b3b66b3d1ba4a9cb176b3bbb9222dd94d1218a0bd018a1b95c406ce6aa`  
		Last Modified: Fri, 14 Nov 2025 01:42:33 GMT  
		Size: 220.4 MB (220429816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0bde317f276e615ec0cd3b459a2bd49819311536d717130b78f56c44ed0ee4`  
		Last Modified: Wed, 17 Dec 2025 20:07:40 GMT  
		Size: 25.5 MB (25462097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f57ae75504056c680c5d2c7271369f41c6db71a2bd4530f61b5bb3cef1a6e0b`  
		Last Modified: Wed, 17 Dec 2025 20:07:38 GMT  
		Size: 9.3 MB (9312244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810d02f9a55b4f56c42dc80e672257b14b3ac92faf2d6d4f556219deca9fb100`  
		Last Modified: Wed, 17 Dec 2025 20:07:37 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6624451a6947299d65e91fe93d23be34487b2156d37fcea2c95442d30e6a8ad0`  
		Last Modified: Wed, 17 Dec 2025 20:07:37 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:9258f1aa29ec3ede6e5f6245f95396ced380c775ae7b9bd1fe84e490ec4960b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4328421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c58a92b2b5aaed47fa2e9aa1f5dc3b498118908e6e991b914aba904ba888c1d`

```dockerfile
```

-	Layers:
	-	`sha256:f0845bbaa7a1c345e51ef883464c7284fc2d686d3af1cf399513cee2bfed6ce2`  
		Last Modified: Wed, 17 Dec 2025 21:34:29 GMT  
		Size: 4.3 MB (4310676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8943a0fa994f1e4ad86df251481ba4d4d0625abf5fef0edce08ab8b27c5dd40`  
		Last Modified: Wed, 17 Dec 2025 21:34:30 GMT  
		Size: 17.7 KB (17745 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:sapmachine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:60ea490689b24e1edd979be3a177240a9392bd533bd7335ecc026b06d0476006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.9 MB (281893956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8cc79b802d57c423d5450fc98cde00ae0dd4b03a4300f710612152f75c9af9`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:42 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 13 Nov 2025 23:36:42 GMT
CMD ["jshell"]
# Wed, 17 Dec 2025 20:09:50 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 20:09:50 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 17 Dec 2025 20:09:50 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:09:50 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:09:50 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 17 Dec 2025 20:09:50 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 17 Dec 2025 20:09:50 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 17 Dec 2025 20:09:50 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 17 Dec 2025 20:09:50 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 17 Dec 2025 20:09:50 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 17 Dec 2025 20:09:50 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 17 Dec 2025 20:09:50 GMT
ARG USER_HOME_DIR=/root
# Wed, 17 Dec 2025 20:09:50 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 17 Dec 2025 20:09:50 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 17 Dec 2025 20:09:50 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6010e2e23970c6d32ac7f316bbae37bc4c141bff6adc9b6d7037a709f7cc4c`  
		Last Modified: Fri, 14 Nov 2025 02:00:00 GMT  
		Size: 218.2 MB (218186634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d8524ead11df45a3fe7e7a1618c645bc1f665f8141815cfe6b7ddfd47a4167`  
		Last Modified: Wed, 17 Dec 2025 20:10:12 GMT  
		Size: 25.5 MB (25532089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560448d28166ed38e1b55b82e866b3fc29f0b81c9a3061896b3bfecb4f32f409`  
		Last Modified: Wed, 17 Dec 2025 20:10:10 GMT  
		Size: 9.3 MB (9312238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636b244d4a7e8a81a2d4371e9341463663804be6973802dead442c5b37067f10`  
		Last Modified: Wed, 17 Dec 2025 20:10:09 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9871c95825666d6f1d23d8c79fe98a193220f73121b1df3d48d73366b4d3d5c3`  
		Last Modified: Wed, 17 Dec 2025 20:10:09 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:230e66e8c2d5ea648024bd525b23da0624c9ffbaa9da18193f8f2ad15216a70f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4335168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd9103f9312d6809df3cf88868dcc0fc73552a2796dd79716d58ce20e3c7306`

```dockerfile
```

-	Layers:
	-	`sha256:e0c402280bb7005f9e106dff31c28e0b9411eb82a8ce28c188bb6f2404ccf127`  
		Last Modified: Wed, 17 Dec 2025 21:34:36 GMT  
		Size: 4.3 MB (4317243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21424476a2d7b7e3d911198d88b6816f6dabda7a5437eac7c12eba23edc186fd`  
		Last Modified: Wed, 17 Dec 2025 21:34:37 GMT  
		Size: 17.9 KB (17925 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:sapmachine` - linux; ppc64le

```console
$ docker pull maven@sha256:4449299d7f33340b32c6dc72d5b973ffbf2922c960cbab64e9911c4070ffbc6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.9 MB (294863289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bddb43cd9d15bed0c3d91374742159cb52b78b8eeff86e172c1e9ad25291c4f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 01:09:27 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:09:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Fri, 14 Nov 2025 01:09:27 GMT
CMD ["jshell"]
# Wed, 17 Dec 2025 20:23:50 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 20:23:51 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 17 Dec 2025 20:23:51 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:23:51 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:23:51 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 17 Dec 2025 20:23:51 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 17 Dec 2025 20:23:51 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 17 Dec 2025 20:23:52 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 17 Dec 2025 20:23:53 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 17 Dec 2025 20:23:54 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 17 Dec 2025 20:23:54 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 17 Dec 2025 20:23:54 GMT
ARG USER_HOME_DIR=/root
# Wed, 17 Dec 2025 20:23:54 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 17 Dec 2025 20:23:54 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 17 Dec 2025 20:23:54 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Tue, 16 Dec 2025 00:07:47 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74879aa2e7aa3e8dd90675709cdfb401241c677206a6b1298cf477a866094644`  
		Last Modified: Sat, 15 Nov 2025 06:51:10 GMT  
		Size: 221.3 MB (221259256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3655fdd0887a5581c3ee6af4e1845c82bb043c98c3adc84beb51d71a39fada`  
		Last Modified: Wed, 17 Dec 2025 20:24:44 GMT  
		Size: 30.0 MB (29986334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80885b42e64da7a7fdd6780d8dbf1d4a9663eced4399ed098308c901c49592f2`  
		Last Modified: Wed, 17 Dec 2025 20:24:42 GMT  
		Size: 9.3 MB (9312237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30f36727ad8f7dabc86680f6303d7acfd619f872a3e93e486aa84a42279aea0`  
		Last Modified: Wed, 17 Dec 2025 20:24:41 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ad1b935d9a3c93f784cc0eaf4954b5774920d489d26fc748e633e322785ee6`  
		Last Modified: Wed, 17 Dec 2025 20:24:41 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:6379bed92955df7e634f6323aba2160d4cdad4550fb1072d46d8fe3b8e54e8ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4326913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850ff8a4b70998409f02f684114dfc9ea124d8aad4acba3fdb997d8193ef77ba`

```dockerfile
```

-	Layers:
	-	`sha256:ae3eb4405f86f9a5274ecb928396ac4d8cf88e457a224404318b713276cc3140`  
		Last Modified: Wed, 17 Dec 2025 21:34:42 GMT  
		Size: 4.3 MB (4309094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:151acf736bfd46c1372373169795f00d67fff8757c4ef368e05b2c276b4c383a`  
		Last Modified: Wed, 17 Dec 2025 21:34:42 GMT  
		Size: 17.8 KB (17819 bytes)  
		MIME: application/vnd.in-toto+json
