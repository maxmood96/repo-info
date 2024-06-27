## `maven:3-sapmachine-22`

```console
$ docker pull maven@sha256:2c65277d3daf5553f7f1ff48e60ece0d5875ca623b1425aa28206cb70259763a
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
$ docker pull maven@sha256:eebce840a151ca61d22d35c6de698cf0ba5577875d3291c7c7a26e2ce0204219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274092069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2d51f1c0c8319989c48e0562e8c1c496fd3d47a8dabf4975fce942fd81ee38b`
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
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
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
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8be052ef5d257bce29bcdac702f21606f8f820cb3a9f5c2aaec6f245d396016`  
		Last Modified: Tue, 25 Jun 2024 23:50:20 GMT  
		Size: 211.8 MB (211781332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b35db3838ce1b1b0830f4e0861ae3f47e8276c9562fedeff00d097ae96258d`  
		Last Modified: Wed, 26 Jun 2024 01:28:32 GMT  
		Size: 23.8 MB (23819032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39aa65a93db7f1f0bbc52ef2198a2ff037455e98f770481efbe179a882307c24`  
		Last Modified: Wed, 26 Jun 2024 01:28:31 GMT  
		Size: 9.6 MB (9647617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9e5939001cd19e6fe2c1f0e7666c64bb1513803d218b1121a540d5b4993d3f`  
		Last Modified: Wed, 26 Jun 2024 01:28:31 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ca4f54735525bf55ddc3ceffff5d1ac52f4dcbd670d990f736823f6a15a13e`  
		Last Modified: Wed, 26 Jun 2024 01:28:31 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-22` - unknown; unknown

```console
$ docker pull maven@sha256:ae694151db9e2b68f078eda552a833158e698d1aa9af164d38717d292d854855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4071246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58071ea397a080a579797533d9815d17cc496057c0fa3337da5dfda66568716e`

```dockerfile
```

-	Layers:
	-	`sha256:cb12907da591dfd8e33966ba4061f88838d7a1bca368a1ed3a622016d0d97f4f`  
		Last Modified: Wed, 26 Jun 2024 01:28:31 GMT  
		Size: 4.1 MB (4054052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a48ae46296963b0df21ef5d15639cadc4850ffd3e5c0a0107ae319e369461526`  
		Last Modified: Wed, 26 Jun 2024 01:28:31 GMT  
		Size: 17.2 KB (17194 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-22` - linux; ppc64le

```console
$ docker pull maven@sha256:333717e066421964ed51cc91deb8209d0bfba8c40ce7430f9d409ff9d1b18154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286524625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802ba3ad3cd4f680d5849542902b03f2b74321d5caae8494196a2afa0458b9ac`
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
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
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
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccc34635659453a00507f117554b35de0cc6055a7e9f1d9d5e220ab8d70f5ca`  
		Last Modified: Wed, 26 Jun 2024 00:06:30 GMT  
		Size: 215.0 MB (214996096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005e301411736b41b91244a5c793f89fb38d21138580f554bc0df8d9fed9c9b7`  
		Last Modified: Thu, 27 Jun 2024 19:13:43 GMT  
		Size: 27.9 MB (27859673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0ec3270d5dc4b2e1269d57243e059f2f12b82a894a8610f2bec852bf494d28`  
		Last Modified: Thu, 27 Jun 2024 19:13:43 GMT  
		Size: 9.2 MB (9161782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9107454f39bc6b66a51bd23bd9e1ca77af904614e5d27ff5c891ff0f5fa5e4`  
		Last Modified: Thu, 27 Jun 2024 19:13:42 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc95700e72527ac65427b86e8f3f8c7359104ba83083f8657920f6142d42df6b`  
		Last Modified: Thu, 27 Jun 2024 19:13:42 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-22` - unknown; unknown

```console
$ docker pull maven@sha256:c22fcb8907b48776648d487f420406d00d0351e6b31b41629cb02a064634a361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4068872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2663eedb15688796c633e73522012471f7b2487815a6db5aa5ed18ee9c46035e`

```dockerfile
```

-	Layers:
	-	`sha256:0455b0caebb15a9e638ff43b657085228718f0e3cb5d43a0103b1febf172c44b`  
		Last Modified: Thu, 27 Jun 2024 19:13:42 GMT  
		Size: 4.1 MB (4052323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2be37166a14da692eb9e48073e39fc44d935572d3b0ee35de81f8f7fcde1d0eb`  
		Last Modified: Thu, 27 Jun 2024 19:13:42 GMT  
		Size: 16.5 KB (16549 bytes)  
		MIME: application/vnd.in-toto+json
