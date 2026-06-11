## `maven:3-amazoncorretto-17-debian`

```console
$ docker pull maven@sha256:6526cde4b7ef17320b1e92090f2062c92d7f59bbcca782b47e446b8f39c777b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-debian` - linux; amd64

```console
$ docker pull maven@sha256:4f802224615c1108ededd7d269411840e2ff56f5a7f3a23431aec178028e9dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240916041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84621e16f8049ee52dd88817cdcb1f1a9d8202d6974ca7dc7fd9ca1d4026f5f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:23:06 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:23:06 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 01:23:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 11 Jun 2026 01:23:06 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 11 Jun 2026 01:23:06 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 11 Jun 2026 01:23:06 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 11 Jun 2026 01:23:06 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 11 Jun 2026 01:23:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 11 Jun 2026 01:23:06 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 11 Jun 2026 01:23:06 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 11 Jun 2026 01:23:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 11 Jun 2026 01:23:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 11 Jun 2026 01:23:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 11 Jun 2026 01:23:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 11 Jun 2026 01:23:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f1913edea6458f75bd054184e670506c73f40a0b226e3eccad5ecce1626236`  
		Last Modified: Thu, 11 Jun 2026 01:23:30 GMT  
		Size: 201.8 MB (201769663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd6250be40933b0ac02313a26362e9cf7d34d9273d0af7d7149d51266399610`  
		Last Modified: Thu, 11 Jun 2026 01:23:25 GMT  
		Size: 9.4 MB (9359958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039bf74d15718af03ede132365206fb7904cf589a5adaa5960f8f1dff6810184`  
		Last Modified: Thu, 11 Jun 2026 01:23:24 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1381f75f5e112494c6381d021d2a7cbbef434aa2d7369dac5977004437d63c`  
		Last Modified: Thu, 11 Jun 2026 01:23:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian` - unknown; unknown

```console
$ docker pull maven@sha256:659fec8b7174c6c0c09927551426d32e911e605440ab825e623d38794dff64e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7f0948b7b3259579bb7e25f6bb20320ce2df6a84088b2d7bc946eb51b02ec7`

```dockerfile
```

-	Layers:
	-	`sha256:2243d656f6f5880c63ff1a3b767c688756d173315b45ad81f07a9416ea0c8733`  
		Last Modified: Thu, 11 Jun 2026 01:23:25 GMT  
		Size: 3.1 MB (3104886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b522c984433c522b0c0318f113856ddf17a34473cf5938ced70e379ce4ddce39`  
		Last Modified: Thu, 11 Jun 2026 01:23:25 GMT  
		Size: 17.5 KB (17525 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:555ca5a9ac92f20bfb44ceb998203577f9baf3c21cbcdc14e4d98a404211f878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.8 MB (239815681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9383d5ff854597a2b689dde55d8ba7d4b37533a3758fe1a1d8993d4d2f5031`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:27:20 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:27:20 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 01:27:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 11 Jun 2026 01:27:20 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 11 Jun 2026 01:27:20 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 11 Jun 2026 01:27:20 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 11 Jun 2026 01:27:20 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 11 Jun 2026 01:27:20 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 11 Jun 2026 01:27:20 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 11 Jun 2026 01:27:20 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 11 Jun 2026 01:27:20 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 11 Jun 2026 01:27:20 GMT
ARG USER_HOME_DIR=/root
# Thu, 11 Jun 2026 01:27:20 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 11 Jun 2026 01:27:20 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 11 Jun 2026 01:27:20 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:424da253d9b1d803755be01196f0dc044886c057821acb7f0ad16b8632c8cd35`  
		Last Modified: Thu, 11 Jun 2026 01:27:46 GMT  
		Size: 200.3 MB (200306184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6975d44dfc71b7863e84a50bb09cc8b53f80d2acb873d24934dd81a92ba4ca1c`  
		Last Modified: Thu, 11 Jun 2026 01:27:39 GMT  
		Size: 9.4 MB (9359963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff3ddd9b3f45cb41b47bb20627478b73966dfc0d90729ba1a1d46c29a04f7810`  
		Last Modified: Thu, 11 Jun 2026 01:27:39 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602a2a3c6ca3c30c6bb1ceaa640d268d83d12451c179297c7d50fa65327597b0`  
		Last Modified: Thu, 11 Jun 2026 01:27:39 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian` - unknown; unknown

```console
$ docker pull maven@sha256:a21210324483c4cc3c827ed82ca31326715d019cbcce51eb9522a61def9582c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a40da7a5158869ddb87e9d9caeece3f7fc60c5662d2efae667de9364bafeaaad`

```dockerfile
```

-	Layers:
	-	`sha256:67fdce470c11027ae27721db0b9f38173dca5f828379e79f8b66185e131aac03`  
		Last Modified: Thu, 11 Jun 2026 01:27:39 GMT  
		Size: 3.1 MB (3104541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:132f84db9beaacf4a04d65b95ab033b52e47e526696d05b425abf5ceecfd3b39`  
		Last Modified: Thu, 11 Jun 2026 01:27:39 GMT  
		Size: 17.7 KB (17694 bytes)  
		MIME: application/vnd.in-toto+json
