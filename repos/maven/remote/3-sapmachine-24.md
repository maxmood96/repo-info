## `maven:3-sapmachine-24`

```console
$ docker pull maven@sha256:7bf3d4742e4fb9a81c8b672c4bfcea5e2740af6a2a17238aaabaf6ac762aa7bc
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
$ docker pull maven@sha256:4e408ba4b67a25324e3012daa3661dff28ce1937974184fa9a7ff9c32cf54d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.7 MB (296735164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce0240f1cd5278eafd566cb823c4b8ea2eeed98be1fc35a298decd18ac690948`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
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
	-	`sha256:3437ed35f5c8d446cef703f6d9da0457dbfb86de2d1c0bf4dddc4f47150e8a1d`  
		Last Modified: Wed, 09 Apr 2025 01:20:35 GMT  
		Size: 232.4 MB (232393884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e373d1e9c7422ffc21cba80fe53867a7005b445821daae771621aa3b48bc59c`  
		Last Modified: Wed, 09 Apr 2025 03:13:26 GMT  
		Size: 25.5 MB (25452146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85d664d023b3823888bf45d6eb4017443f188251228be44e0ca276555101ffe`  
		Last Modified: Wed, 09 Apr 2025 03:13:26 GMT  
		Size: 9.2 MB (9170445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6091a6583326e492b0db00b6b6d99a5f38bf3f3174c640d5f5510ddc9e23405a`  
		Last Modified: Wed, 09 Apr 2025 03:13:25 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948f420ec919bcdadddc3873187552e6fe01dceff560d3b59347f7d82901428b`  
		Last Modified: Wed, 09 Apr 2025 03:13:25 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-24` - unknown; unknown

```console
$ docker pull maven@sha256:36be34328f2b364e2a85ec6ca9aeabc9ee91481a63536cf4f63f8a676ce2f0a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4165088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2408c571e9859a306630de2f1ec5cf546470bd636b023b3b72329b5d73439f5d`

```dockerfile
```

-	Layers:
	-	`sha256:9231de15dec53ba4afd0177798dc7a36d23803ad161c27c3bfdc37add25149be`  
		Last Modified: Wed, 09 Apr 2025 03:13:25 GMT  
		Size: 4.1 MB (4148550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a00a4b3bad9b415c5ce6e1dfe82884a80baa1f97179780dfa9c2cc40d5ff69d7`  
		Last Modified: Wed, 09 Apr 2025 03:13:25 GMT  
		Size: 16.5 KB (16538 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-24` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:3270bab223c5488c3318ea6ba9807e9a9eaca9e7962ddf865a2d79491d998efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298525528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313814a82715c028a7071ab6e6e4e013c4deb33b25f3d7bc6081a8621c25f8f6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
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
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11c53936a49f11dab09db667c9f6380067a86be449f9ece0bfd550a497645a5`  
		Last Modified: Wed, 19 Mar 2025 20:33:03 GMT  
		Size: 232.6 MB (232556928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1df5dc27fa009ebc1d3c52a94f597e82798e29697aa7a64a545b47995e5bbbe`  
		Last Modified: Thu, 27 Mar 2025 20:30:24 GMT  
		Size: 27.9 MB (27903525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7bec9ade4a384695e8c21be9842f34cb1bde2aa0762f349b9c286936d869a1`  
		Last Modified: Thu, 27 Mar 2025 20:30:24 GMT  
		Size: 9.2 MB (9170437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7f6bbfa577b6491f8e316c6721ca8a033efa714307a07e6ed222fd9768a82b`  
		Last Modified: Thu, 27 Mar 2025 20:30:23 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7d5f329bc7369b1ac4f95ef01d43c612f8aede77eb341634a070764aafc55f`  
		Last Modified: Thu, 27 Mar 2025 20:30:23 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-24` - unknown; unknown

```console
$ docker pull maven@sha256:3c3dd905c175104dcab909e7c921ebfbdc864be5b1d45b3ccc0e6cac65a46c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4173926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42369e44f1609feee4b063281f2a405c0b21058df045eb9e7ea837f88b0ec74`

```dockerfile
```

-	Layers:
	-	`sha256:c0462117061c0c6065f736d367d9cd35365590ab71008f2e32c913c27b58ee85`  
		Last Modified: Thu, 27 Mar 2025 20:30:24 GMT  
		Size: 4.2 MB (4157254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cdeded3e2e6ba5b9b5321d070277723971b99186db096ecbf08207e2f617706`  
		Last Modified: Thu, 27 Mar 2025 20:30:23 GMT  
		Size: 16.7 KB (16672 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-24` - linux; ppc64le

```console
$ docker pull maven@sha256:53e1721cc0f1e151f16a6ccf86b9aecba3fc1749590c44ebd72e5a829150774a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.2 MB (307231595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e96d41c3b8a9522b9aeb3a4ede6c7b8234e80ad672a1fdffd6d9849c586304`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
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
	-	`sha256:99dbed487d09d89c96ca9a6f11775281f704f98f496f1ecd9800b0596428fb45`  
		Last Modified: Wed, 09 Apr 2025 06:32:47 GMT  
		Size: 233.7 MB (233732026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef005f8eee882aabf0bd8ac3482cee7b6e88c5b82493a2c0488fbe33d403e67`  
		Last Modified: Wed, 09 Apr 2025 15:58:15 GMT  
		Size: 30.0 MB (29987225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6d7a414cc0cd11edec33090af43375711e6fd7bf7b373d69ebefdaf88fac2a`  
		Last Modified: Wed, 09 Apr 2025 15:58:14 GMT  
		Size: 9.2 MB (9170437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ed9ff5908506a496c26891c25c8eb3295cbccc1cd13ce7eeb176af6964d216`  
		Last Modified: Wed, 09 Apr 2025 15:58:14 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8e0095cae356d3137a2a85a7c8590197e197091257109b4d3ccb49e6c5214c`  
		Last Modified: Wed, 09 Apr 2025 15:58:14 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-24` - unknown; unknown

```console
$ docker pull maven@sha256:80b9d59ed9ab4ddd891a92606411a8bff34c8846c8eb0134b1c51d50ec7598a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4169375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a9818e2fbfa1eb6bd946354e0ad962ddd55be0fc7e18f4b1479469b1916afb`

```dockerfile
```

-	Layers:
	-	`sha256:5afa183d05ce8c1da3538ec676125689a5ff9480df7fe61d004d304ec148d4df`  
		Last Modified: Wed, 09 Apr 2025 15:58:14 GMT  
		Size: 4.2 MB (4152786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62f4decaeeb227cabf9ddd285cb77bf9c4f1c9f4f48315463b9fd1c31f2393b0`  
		Last Modified: Wed, 09 Apr 2025 15:58:13 GMT  
		Size: 16.6 KB (16589 bytes)  
		MIME: application/vnd.in-toto+json
