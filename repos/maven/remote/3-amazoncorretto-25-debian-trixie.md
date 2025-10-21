## `maven:3-amazoncorretto-25-debian-trixie`

```console
$ docker pull maven@sha256:89d86c2a39d99bea3ef2e82b6c2ea072e9372b97336eb873e6c3403bf9a8ea4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:5b2af4671f097c3a9c3483e3b7744a4293ddeaefb86f0861f9a641952fba3391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.7 MB (276732817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cc0bb66549ba166339e7712fb0ae7f40745df341c8e1d7e4f39dd45ffb6606`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 19 Sep 2025 20:50:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Fri, 19 Sep 2025 20:50:17 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-25-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Sep 2025 20:50:17 GMT
ENV LANG=C.UTF-8
# Fri, 19 Sep 2025 20:50:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 19 Sep 2025 20:50:17 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 19 Sep 2025 20:50:17 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 20:50:17 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 20:50:17 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 19 Sep 2025 20:50:17 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 19 Sep 2025 20:50:17 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 19 Sep 2025 20:50:17 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 20:50:17 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 19 Sep 2025 20:50:17 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 19 Sep 2025 20:50:17 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 19 Sep 2025 20:50:17 GMT
ARG USER_HOME_DIR=/root
# Fri, 19 Sep 2025 20:50:17 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 19 Sep 2025 20:50:17 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 19 Sep 2025 20:50:17 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d400bca4eed6f1e7c56da1c3db7f15722475a96fb67a8bdbbe697500b6bfeaab`  
		Last Modified: Fri, 10 Oct 2025 06:01:13 GMT  
		Size: 237.7 MB (237711429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a4724210620a949987fb4f59692feb402e055c6b2caf928e9a139a504ae10f`  
		Last Modified: Thu, 09 Oct 2025 22:54:29 GMT  
		Size: 9.2 MB (9242586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7c52fab9dcceb23273952cfa3be8368ad7d989411cf15f19706af8f97bd707`  
		Last Modified: Thu, 09 Oct 2025 22:54:20 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8b7133af3491995769b8f064c6078be2beeb2465cefa805547e457de4a1491`  
		Last Modified: Thu, 09 Oct 2025 22:54:20 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:93c607e1bf042bc8a68e9ea79c3cfd6ba875956bd3ffc6bbf7fe46b504c3661b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3129649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88dfa7fc4fc3fe58ae67ca5c1d5d9d75f63f47217864e9661cc46b81c2ef4c8a`

```dockerfile
```

-	Layers:
	-	`sha256:7934e2b95c5f87e6845639972d307ae51a9c7947083c760ac03b44e07608e030`  
		Last Modified: Fri, 10 Oct 2025 05:30:26 GMT  
		Size: 3.1 MB (3110406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cdeb60e63b6e5d6c48c666d905dd6defba4022988eca11bf3a2942bcf880a0b`  
		Last Modified: Fri, 10 Oct 2025 05:30:27 GMT  
		Size: 19.2 KB (19243 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:1f43d58960cadbef5a8008235de650d6a2baab035c7639034157a0425fcccf17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271841409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c114253870c6e76250acca5f7ced3bff90458d6f58d529907339bcf589810d51`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 19 Sep 2025 20:50:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Fri, 19 Sep 2025 20:50:17 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-25-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Sep 2025 20:50:17 GMT
ENV LANG=C.UTF-8
# Fri, 19 Sep 2025 20:50:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 19 Sep 2025 20:50:17 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 19 Sep 2025 20:50:17 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 20:50:17 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 20:50:17 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 19 Sep 2025 20:50:17 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 19 Sep 2025 20:50:17 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 19 Sep 2025 20:50:17 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 20:50:17 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 19 Sep 2025 20:50:17 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 19 Sep 2025 20:50:17 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 19 Sep 2025 20:50:17 GMT
ARG USER_HOME_DIR=/root
# Fri, 19 Sep 2025 20:50:17 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 19 Sep 2025 20:50:17 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 19 Sep 2025 20:50:17 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba7e7b34eee9bc6d9debbfe8f5658faa7d2c183d8995633d064716184f244de`  
		Last Modified: Tue, 21 Oct 2025 02:31:10 GMT  
		Size: 232.5 MB (232455652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1409a1690816d207bc3b02193a9fcfc10396c5563e97c028065f9f321547f8`  
		Last Modified: Tue, 21 Oct 2025 02:31:20 GMT  
		Size: 9.2 MB (9242593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb26cabf1627bd9ca7d10d2048f756440f7a65d98ca508edfa9e6129fc831a4`  
		Last Modified: Tue, 21 Oct 2025 02:31:18 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb82c8ddd733e300eed10bfee555e998af08c805ed9089c1e3442a122ad9c6d1`  
		Last Modified: Tue, 21 Oct 2025 02:31:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:b0210e3a9982cda095ef6f9903110504d0ba5bd4dfeae1c41452ab692087a05c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3129477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd803ff5c2ee8036bc688138bc3e3673ee1d01f8e26b796ec4268926103738d1`

```dockerfile
```

-	Layers:
	-	`sha256:c2b7d2324085fc5c2e8697088f252ff9ca18c34dc84aaffb75fb8041f5d91972`  
		Last Modified: Tue, 21 Oct 2025 08:28:04 GMT  
		Size: 3.1 MB (3110066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf1215fceb1be680f590085a23d5800a60739c7bb8de9ebd53aec926fd2c669a`  
		Last Modified: Tue, 21 Oct 2025 08:28:04 GMT  
		Size: 19.4 KB (19411 bytes)  
		MIME: application/vnd.in-toto+json
