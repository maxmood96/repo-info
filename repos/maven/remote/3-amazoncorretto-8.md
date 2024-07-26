## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:62efb854f5c88db9ba8f818601a38227b6aee6bbd700547f30dfba937b46f122
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:b9c4c012b9c09ec4c83a69cb36cd30da2f3f0340555c4f4eb43f55cfdf274aa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.9 MB (292878554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fca34dda8845537057d984a6dd5969bf5034a06a3be2d45b3c005eb84be848b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /rootfs/ / # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
ARG version=1.8.0_422.b05-1
# Thu, 27 Jun 2024 09:17:07 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENV LANG=C.UTF-8
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 27 Jun 2024 09:17:07 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
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
	-	`sha256:78d6b943ec35657899afc44f3f9b766ee923d9028028da721b7d4e7bc35e184f`  
		Last Modified: Tue, 23 Jul 2024 13:50:25 GMT  
		Size: 62.7 MB (62679166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba3e469516848c9e5827a5c193c9649717e5fc70dc9e65985a1ab4065891012`  
		Last Modified: Thu, 25 Jul 2024 21:01:03 GMT  
		Size: 75.6 MB (75568332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cf714fdc7b98433b68fb6348b1372d98226e3607230bc0328c0ed1ef53b51b`  
		Last Modified: Thu, 25 Jul 2024 22:00:59 GMT  
		Size: 145.5 MB (145468203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee900f67db0f8d50d276584539b078139aa05d581f6fdb99293352bbbb6d5d31`  
		Last Modified: Thu, 25 Jul 2024 22:00:57 GMT  
		Size: 9.2 MB (9161812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813d67e2edf295da41a7ceee7bbd107d49b9e05f4e18942304b4ac47e5fd9f75`  
		Last Modified: Thu, 25 Jul 2024 22:00:57 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0450f50869147e83b4242939f5c2289b76e5ab2b4781714e4f50a72351d64480`  
		Last Modified: Thu, 25 Jul 2024 22:00:57 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:ff35adb1f354efe59e452190dfd2dacd07ed0042dbd3fe93d2cd59dbb110c441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5500645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd6b8a394220e624eca2300e0ef1a39f63b563171a0f91e2bc7aa4b389fcf23`

```dockerfile
```

-	Layers:
	-	`sha256:dd2aead8ff0d400b3ac18245ff9d02d7dd36ab3082ee542c77d8941afc0efd1e`  
		Last Modified: Thu, 25 Jul 2024 22:00:57 GMT  
		Size: 5.5 MB (5484370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d46dc4428e3b95ba9efb578e1546df6a3f72decd05fb5c91a31142d6e90a738`  
		Last Modified: Thu, 25 Jul 2024 22:00:57 GMT  
		Size: 16.3 KB (16275 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:59c168895f35a89efdee41735f74b7d4b3c07a96c4928f6c1a8255fc2aa8011d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.8 MB (254778677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:367e672fdf9abd090dc378d5392940dcb019755be357151e2950c559559b1b36`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
COPY dir:cdeeb89e10fdbe3f38b9e5f6d359ee1afb9caaa1018fdd71fd6c0374dc592a5f in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
ARG version=1.8.0_422.b05-1
# Thu, 27 Jun 2024 09:17:07 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENV LANG=C.UTF-8
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 27 Jun 2024 09:17:07 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
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
	-	`sha256:4ba2ef523fa6e28aa5a068ecb9167a3b9efa29481c3ecc6d34fab1c350b98b6d`  
		Last Modified: Thu, 18 Jul 2024 21:40:02 GMT  
		Size: 64.6 MB (64575311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32eb1b24b2c82db919ec9d4ae81fbf5fc35b9434d43b0734066aa19da336490f`  
		Last Modified: Thu, 18 Jul 2024 22:49:44 GMT  
		Size: 59.7 MB (59663921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912183956cce103ce9be2f7ce0edb2ffad341e11505601a66a495c3cfca86d0c`  
		Last Modified: Fri, 19 Jul 2024 00:03:57 GMT  
		Size: 121.4 MB (121376627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2f63e776296bc3dbe3b2a1d49533ef303e8d12531cfbac5e44f88794935755`  
		Last Modified: Fri, 19 Jul 2024 00:03:54 GMT  
		Size: 9.2 MB (9161775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614770b420085d81d6a1acd7ef119eda060ee1023c130cf75a1a4eed4769b679`  
		Last Modified: Fri, 19 Jul 2024 00:03:54 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2350ba4201ddd977d30133521b2e3e4b8ba6266f55b434dbdd0ea44d7ea13ee`  
		Last Modified: Fri, 19 Jul 2024 00:03:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:68d9cf919cda5354f25c00d3f2335e3ed2abe123d775ce780eeea80897f95ec0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5479880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:377e6058fedcfced3e56d33aec7927929266ce389dfb07209ed1b3415fa0f8ec`

```dockerfile
```

-	Layers:
	-	`sha256:a2caa8164d38283f61f9b478a8f52b41ac274eab980ed52e06a6370df64cf35c`  
		Last Modified: Fri, 19 Jul 2024 00:03:54 GMT  
		Size: 5.5 MB (5462845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff7f4bf4a10e2babb82ce915f20509dc6e32b29419cf7f92c26f131c05884f97`  
		Last Modified: Fri, 19 Jul 2024 00:03:54 GMT  
		Size: 17.0 KB (17035 bytes)  
		MIME: application/vnd.in-toto+json
