## `maven:3-sapmachine-24`

```console
$ docker pull maven@sha256:e73424dc73c63aeff7102bd6f503b2ee3be8e1ace1760997a4c5d1878ee9a439
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
$ docker pull maven@sha256:9b0afcb3eec7f9918eeeac89e5f46d20e2cfe41bc3798b418f58bd18ae6e854b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.8 MB (296774678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ac1404aa7bfd9c62f45afe5b0b04809a597a9de36bd5ed132c847cefca6224`
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
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
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
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Thu, 29 May 2025 06:11:31 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f03e71d60a3fd411bf974f1a6a298511beae2ad730d1bfee9aa35eaec780e4`  
		Last Modified: Tue, 03 Jun 2025 04:17:57 GMT  
		Size: 232.4 MB (232429941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52281f9a62b2476a4fa99908f65705148ab75d64103161b42d02d93faf73c82e`  
		Last Modified: Tue, 03 Jun 2025 06:12:53 GMT  
		Size: 25.5 MB (25457926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d685c5511c4d82ab4f918257ddcb1abc4cb779dc2551b26c24b451f662625b0`  
		Last Modified: Tue, 03 Jun 2025 06:12:52 GMT  
		Size: 9.2 MB (9170439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789fdd1623535a30f72942679a931c3ee4c1271fb8726d1f941f5af07dac1459`  
		Last Modified: Tue, 03 Jun 2025 06:12:52 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7c8d01fff48af3eb83b3260e94f4f1f305824ae8349e8c3ab7286d3706193a`  
		Last Modified: Tue, 03 Jun 2025 06:12:52 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-24` - unknown; unknown

```console
$ docker pull maven@sha256:1ed5e65770e8a96491a8bb809e67a31c9bc33abfd40f4c395c504610a880957f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4195656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313d150c1d5ce28946f1f076a6d31339f59424e592bd88149df374ba0195ee9e`

```dockerfile
```

-	Layers:
	-	`sha256:dc2104a0e84a5799b5c45e49b052588154e16fea98a568a7e4857b24c21e2266`  
		Last Modified: Tue, 03 Jun 2025 06:12:52 GMT  
		Size: 4.2 MB (4179117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd20c3af1b0b45eb778378a6a23dc6b55440c154620645963c8baa63ebf12f45`  
		Last Modified: Tue, 03 Jun 2025 06:12:52 GMT  
		Size: 16.5 KB (16539 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-24` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:d622b9b15461e5569f211c1cda5d83fad41098cd0da7fc720119e76b4baaa62e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293909174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b15559c1b3998abb25b384d4b8741c955a2bfdd570a356eaa83e39bcc6324b`
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
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
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
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35487db28eea20818492fde74111801e2c81f72e49c62ff1730d39f0f99fecff`  
		Last Modified: Mon, 05 May 2025 18:23:24 GMT  
		Size: 230.4 MB (230360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e834460f17ed7bbaa64fdd27beadd34b61c2a429471576de34e12765d7d45e26`  
		Last Modified: Tue, 06 May 2025 04:01:31 GMT  
		Size: 25.5 MB (25530794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f7d7d5e152468aa64afc348123f54151089cf1453b00e1b0e8e9982386d10a`  
		Last Modified: Tue, 06 May 2025 04:01:30 GMT  
		Size: 9.2 MB (9170436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa3830d0a3b268cabbd8ea8162c95b8046b8665a5947e6de2f0382b743a86fb`  
		Last Modified: Tue, 06 May 2025 04:01:30 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9103df8a0de623b79bd3dab0bb82b8050fb341498aa303ad1b1341d2c1543be1`  
		Last Modified: Tue, 06 May 2025 04:01:30 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-24` - unknown; unknown

```console
$ docker pull maven@sha256:631767e4843edb54bff78bcd761ae0791339522ec6e24e7a6176e785aa30a15b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4171769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9278f9f32531bf264d02807e0eb6cd1f7452fd85e84b8067b5fedb2131aa4c`

```dockerfile
```

-	Layers:
	-	`sha256:8c9c43c95591bf6dee596cd303a9782e95d9f49908dd1872e0ca8394f66175a2`  
		Last Modified: Tue, 06 May 2025 04:01:30 GMT  
		Size: 4.2 MB (4155097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee49a200fd2270c132f27edef4ed12bc2ffc5da60978462fda0a5c359d54bfe4`  
		Last Modified: Tue, 06 May 2025 04:01:30 GMT  
		Size: 16.7 KB (16672 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-24` - linux; ppc64le

```console
$ docker pull maven@sha256:d706c174cc14a5b042fac818a0c476f8dfe12f6674aa96982fafbed612042c57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.3 MB (307267281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea7acf0432c60c4ef8cf022dc3305a5d55625932a2a723aaf1feaa8db24ee5d1`
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
ADD file:d4d363297b0bc97147d6215ececd915564f3540c035d4c68fcdd781acaf0e4e7 in / 
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
	-	`sha256:fd7ce82c353803b69e06046e91345d15e766766fa395e4fb8e9f652834cddb32`  
		Last Modified: Mon, 28 Apr 2025 10:54:08 GMT  
		Size: 34.3 MB (34340838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9764227cde0adcf55777c13af3bce7c5a28f107cd380ea030884fc2780824f5`  
		Last Modified: Mon, 05 May 2025 18:11:11 GMT  
		Size: 233.8 MB (233770979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98cc5a8e4cf113fa2ce56f52a314f03430f787d1fbc44c8627808b6fc09c1fc0`  
		Last Modified: Tue, 06 May 2025 00:51:23 GMT  
		Size: 30.0 MB (29983980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a13bdf422b7c817d24c83d459d803013ac2d2df67dd577ea77dcd3b4c1aa310`  
		Last Modified: Tue, 06 May 2025 00:51:23 GMT  
		Size: 9.2 MB (9170440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afdb6754aeab6065b9c02fa8d5af23c2dd6da6bdc0c8a477b74e42c82b83a86`  
		Last Modified: Tue, 06 May 2025 00:51:22 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3d3e1d8fc1399571a76a78dd84baa2690df5efaea500660c91605ed646232e`  
		Last Modified: Tue, 06 May 2025 00:51:22 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-24` - unknown; unknown

```console
$ docker pull maven@sha256:1e226f2f58daeece1c1b2f16ab4d1d3c9d6f5065337382de38df6de769f25e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5d910f9e17d35673bf64d968e1e622a45dae4486a2f406b7964e61217a3e91`

```dockerfile
```

-	Layers:
	-	`sha256:4498975f815a5e3b81f4789e5f2bbb7d647dbee582d7ea6fc2f22afa8f35176a`  
		Last Modified: Tue, 06 May 2025 00:51:22 GMT  
		Size: 4.2 MB (4152814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41172f0f6daee3676e7529a6169ca45717557a2ee7536cba948d268c2619ac51`  
		Last Modified: Tue, 06 May 2025 00:51:22 GMT  
		Size: 16.6 KB (16589 bytes)  
		MIME: application/vnd.in-toto+json
