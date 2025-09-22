## `maven:3-sapmachine-25`

```console
$ docker pull maven@sha256:116eeaad1c90f77456715e2e72b5fcef93be4da8122eb58900c51c1ce05fc1d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-sapmachine-25` - linux; amd64

```console
$ docker pull maven@sha256:404d5ccb27b91f77424b4ca229027337c4eac2666fa755692bab6b6956dd723a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.1 MB (298053406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eed9c55acaece8a52e317a04d634d13258d51edddae9bc720bc6fe7fd6d7edf`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
# Fri, 19 Sep 2025 20:27:44 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 19 Sep 2025 20:27:44 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 19 Sep 2025 20:27:44 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 19 Sep 2025 20:27:44 GMT
ARG USER_HOME_DIR=/root
# Fri, 19 Sep 2025 20:27:44 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 19 Sep 2025 20:27:44 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 19 Sep 2025 20:27:44 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e0d94b1583917327229d8b4b4a26396c18ef7e17839dbf460e61d90c4f4b5c`  
		Last Modified: Wed, 17 Sep 2025 21:25:09 GMT  
		Size: 233.6 MB (233624614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2f1da609c9e66f840d65b4b01efd9ac987229654a8f035302043c955bbf1ae`  
		Last Modified: Mon, 22 Sep 2025 17:07:09 GMT  
		Size: 25.5 MB (25461734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4af1716612fac5ad1591cd9ffdda6917c1ccb559bbb768f32df90ad848ab7fb`  
		Last Modified: Mon, 22 Sep 2025 17:07:06 GMT  
		Size: 9.2 MB (9242574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d69832b2e796b078511dbbeaa1aa67390da806073b62064fdd74fb65da2fd6c`  
		Last Modified: Mon, 22 Sep 2025 17:07:04 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a0c092328938f6fd8fd4462d6c423fb7a6b35a9430465aabe7ea5aa049e964`  
		Last Modified: Mon, 22 Sep 2025 17:07:05 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-25` - unknown; unknown

```console
$ docker pull maven@sha256:2da97ce6f45b1e08f8c8d28c5ca9bbc98921c6aee15584c3c088e4e18e2f3c08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db46f8bcb071643b5b6ae4108fb71109cd891a8db69b8fbf25d3ee241fb1251`

```dockerfile
```

-	Layers:
	-	`sha256:f5af3195c9dcdc8158570f29edc85ed0566fa0f26a24ce11383eaac83befb485`  
		Last Modified: Mon, 22 Sep 2025 17:28:35 GMT  
		Size: 4.3 MB (4311337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2999e204a1500202fd42248477da362b05685a8d3aca06062cce99f104901920`  
		Last Modified: Mon, 22 Sep 2025 17:28:36 GMT  
		Size: 16.5 KB (16546 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-25` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:f662f0ce638a66004301fa95c3c9672ee608dfb0b708a0f61456ac6025d86228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295073347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77bfaa721f2a18cd640ac7483fd9be613cec2a8993cfa5962f7a2691175c98c0`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
# Fri, 19 Sep 2025 20:27:44 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 20:27:44 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 19 Sep 2025 20:27:44 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 19 Sep 2025 20:27:44 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 19 Sep 2025 20:27:44 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 19 Sep 2025 20:27:44 GMT
ARG USER_HOME_DIR=/root
# Fri, 19 Sep 2025 20:27:44 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 19 Sep 2025 20:27:44 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 19 Sep 2025 20:27:44 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba25b8960d63aa2c367d9d67db7a5b21dc33b8157ff6c405c47662ee2727c0bb`  
		Last Modified: Wed, 17 Sep 2025 18:10:51 GMT  
		Size: 231.4 MB (231436131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366e17c6345b75497016d6d135500971fbd94c0b26e5e08205bd985e1b2f8513`  
		Last Modified: Mon, 22 Sep 2025 17:07:09 GMT  
		Size: 25.5 MB (25532273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151af0bf5676192542c471ab38efeb95c91032fbbace93a8813e3e577dc8f3c7`  
		Last Modified: Mon, 22 Sep 2025 17:07:07 GMT  
		Size: 9.2 MB (9242588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8b0dc903e9b7b26edf0254327993c407195ecc2ac86827d5bb821cc0ac95b8`  
		Last Modified: Mon, 22 Sep 2025 17:07:05 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423be2624c27a67e50c8de4c3a8859595898ed43e252bdcc226678d8c2ad6836`  
		Last Modified: Mon, 22 Sep 2025 17:07:06 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-25` - unknown; unknown

```console
$ docker pull maven@sha256:d076080d573287998e17bd53084a5a4b7dd8344ed1e117cea87a817b2bb47703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4334535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6856a82ab29727ee7ce05dec1e7eb364bb1cc596b64c6baa8818bd0d57fd09d4`

```dockerfile
```

-	Layers:
	-	`sha256:081a7d655bb63adcac26e8e4e453406652298dca012ca3da49ae1e96d76950b0`  
		Last Modified: Mon, 22 Sep 2025 17:28:41 GMT  
		Size: 4.3 MB (4317856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:478d701b6a5513d8816b91379eb5a9bebbea47440f2c20eacaf418cf3e297d70`  
		Last Modified: Mon, 22 Sep 2025 17:28:42 GMT  
		Size: 16.7 KB (16679 bytes)  
		MIME: application/vnd.in-toto+json
