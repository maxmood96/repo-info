## `maven:3-amazoncorretto-21-debian-trixie`

```console
$ docker pull maven@sha256:071443f42bb5669cee04139757b23b46fb868ffcfe57dc1c0245b188a372bbbd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:41fe043e75bf2c88556a20ca20e5bdb49adf98008608b8a3cdf6d732b7f54bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255688953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a75a223524af9f9e005808f2578d93247b0d7ce5c8d6d340a18c1787d6e9891`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:42:30 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:42:30 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 03:42:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 13 Jan 2026 03:42:30 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 13 Jan 2026 03:42:30 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 13 Jan 2026 03:42:30 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 13 Jan 2026 03:42:30 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 13 Jan 2026 03:42:30 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 13 Jan 2026 03:42:30 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 13 Jan 2026 03:42:30 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 13 Jan 2026 03:42:30 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 13 Jan 2026 03:42:30 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 13 Jan 2026 03:42:30 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 13 Jan 2026 03:42:30 GMT
ARG USER_HOME_DIR=/root
# Tue, 13 Jan 2026 03:42:30 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 13 Jan 2026 03:42:30 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 13 Jan 2026 03:42:30 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d7d542a837add269a18cdc70aa64e47ff5d8d40d6c9f4133315f8e3fea6e3e`  
		Last Modified: Tue, 13 Jan 2026 03:45:19 GMT  
		Size: 216.6 MB (216601994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea29ce451bc01e9eae846f7bfcbf40f38f853be554a308c7450623f27aeef54`  
		Last Modified: Tue, 13 Jan 2026 03:43:00 GMT  
		Size: 9.3 MB (9312238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a877bf1572a39a1b5a7a0656d298608ee249c63451ec04673e99404593529e74`  
		Last Modified: Tue, 13 Jan 2026 03:43:01 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a8d0ce1d9038634e16b5bf538ba3562f7dee0c684b2d0b4d3a1c388612b0dd`  
		Last Modified: Tue, 13 Jan 2026 03:42:59 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:a5933786926776f2066a0fd8fba6e70b8146ac05c3d92f312bf8c216a16a8679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3123125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b02f4c3aeaac0d55fde2b4f87097e8c329ca74ca6807b71defa9bf93a5189d4`

```dockerfile
```

-	Layers:
	-	`sha256:a00c9060e8338bee87e2e54eacebe50d3033b606bd52cb2686b5108673866154`  
		Last Modified: Tue, 13 Jan 2026 06:29:52 GMT  
		Size: 3.1 MB (3103926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49b0ddfffbd7d47f1246c9ec56a90d76421036657824c72493a83c546944c98c`  
		Last Modified: Tue, 13 Jan 2026 06:29:53 GMT  
		Size: 19.2 KB (19199 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:a8824c45a061ef735582d63f6ab6728b48778b06a3a3d05a514249507ab56ae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 MB (254002875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c662ea84746b4747d468198a81d9ae40fd4728c615b81d1bb99623c8d7a172`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:45:42 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-21-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:45:42 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 03:45:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 13 Jan 2026 03:45:42 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 13 Jan 2026 03:45:42 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 13 Jan 2026 03:45:42 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 13 Jan 2026 03:45:42 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 13 Jan 2026 03:45:42 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 13 Jan 2026 03:45:42 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 13 Jan 2026 03:45:42 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 13 Jan 2026 03:45:42 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 13 Jan 2026 03:45:42 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 13 Jan 2026 03:45:42 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 13 Jan 2026 03:45:42 GMT
ARG USER_HOME_DIR=/root
# Tue, 13 Jan 2026 03:45:42 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 13 Jan 2026 03:45:42 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 13 Jan 2026 03:45:42 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba823fa5e56e8cf16d0a2622150d8647163407848c1e650a1fef6131b1c32d3f`  
		Last Modified: Tue, 13 Jan 2026 03:48:36 GMT  
		Size: 214.6 MB (214555549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e732f25ed170eac8a7824758c5a49215569d56888d11e9043e6c072daf4504`  
		Last Modified: Tue, 13 Jan 2026 03:46:14 GMT  
		Size: 9.3 MB (9312246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f95c8595fb73534789a958515748611365cf732cba65db4e672efcd9caab4c`  
		Last Modified: Tue, 13 Jan 2026 03:46:13 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df62c0a1b50a4b4fb8b3f02e410e9d628ae17fae263ead4c21edc3c9b23d342e`  
		Last Modified: Tue, 13 Jan 2026 03:46:13 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:213e312ea868e2ee8d0bb4b4cfc9bd975bc44301491450078a2cd5393e798068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386cab6ba467de2fd39232bd174dab03159366630fc644af9f26093a733d9be7`

```dockerfile
```

-	Layers:
	-	`sha256:4671b0e485f4e0fb5cc7a805e305a84387c1f0a76f0602c202e90e8c4f2fff12`  
		Last Modified: Tue, 13 Jan 2026 06:29:57 GMT  
		Size: 3.1 MB (3103589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fcc885b7ac87d35b4173c45111a596c24e8e8f5296e938b9662b3ff33309ce2`  
		Last Modified: Tue, 13 Jan 2026 06:29:58 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json
