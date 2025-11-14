## `maven:3-amazoncorretto-8-debian`

```console
$ docker pull maven@sha256:44ff9657d635e4c6fae77593e495ea2cf572530f63f6bd375b912cc3106851ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-debian` - linux; amd64

```console
$ docker pull maven@sha256:0c565f49e2174ebf260de7c2de896b464de3ad273de75d2512a636c8b2efc140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164612512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7d110a40dea69999cb918512555f6399085e27840db5760e767aabaf16dfa73`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 01:42:56 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:42:56 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 01:42:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Fri, 14 Nov 2025 01:42:56 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 01:42:56 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:42:56 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:42:56 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 01:42:56 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 01:42:56 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 01:42:56 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:42:56 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 01:42:56 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 01:42:56 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 01:42:56 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 01:42:56 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 01:42:56 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 01:42:56 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5146cb7fa0cd968f30bd3dc98eb9ceebeba4e383ed2e82d57da0bf9c8312b1`  
		Last Modified: Fri, 14 Nov 2025 01:43:34 GMT  
		Size: 125.6 MB (125590795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff6eaafb114d7bca8625ddc26880b8f0938975357aae9b5e7eef2e29f04bf2e`  
		Last Modified: Fri, 14 Nov 2025 01:43:20 GMT  
		Size: 9.2 MB (9242576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf07a0683c05ffcc480ec836daf7c5445e9eecf8d7bf4c278b0d5abf1978ab6`  
		Last Modified: Fri, 14 Nov 2025 01:43:19 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d9e73b1d17d4bd4eff73eaf25d7763d9632e73de73e7d85b782969cc92bad9`  
		Last Modified: Fri, 14 Nov 2025 01:43:19 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian` - unknown; unknown

```console
$ docker pull maven@sha256:c92f35a430572ce035faabe1155d0f579e40c2adc4a2fed40294948096360bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3001184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d198dcb9e2868929acb30875d4d43685a128fbe564c4803d01e8ac0a0e6803b`

```dockerfile
```

-	Layers:
	-	`sha256:f7f481b56cb5325cd77f765f274043156831d23e12497b8b2008d87274f4ccb6`  
		Last Modified: Fri, 14 Nov 2025 03:29:13 GMT  
		Size: 3.0 MB (2981972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ca847eff852be05e5860b83c0ee9675a2ab8a320020f4dc4cd0caa57cef6183`  
		Last Modified: Fri, 14 Nov 2025 03:29:13 GMT  
		Size: 19.2 KB (19212 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:cf6228ea87a116effc56d57f637437fe019da44e8b0ba1aa6a58488e3ef28d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (148952105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b04b9b7e541f90a1f13403f19bdeb333e2e45b3499555a93ed12c1e87676425a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 01:59:41 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:59:41 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 01:59:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Fri, 14 Nov 2025 01:59:41 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 01:59:41 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:59:41 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 01:59:41 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 01:59:41 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 01:59:41 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 01:59:41 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 01:59:41 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 01:59:41 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 01:59:41 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 01:59:41 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 01:59:41 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 01:59:41 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 01:59:41 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0840c2a43d1462c1f98ff7aeb637563fc38e708a10a0868ffff03905d2350605`  
		Last Modified: Fri, 14 Nov 2025 09:47:10 GMT  
		Size: 109.6 MB (109566194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158d55a2a8dcc034bac207f7ae8fa6deabe5227b2fd088dbd537fd0256af9ef8`  
		Last Modified: Fri, 14 Nov 2025 02:00:08 GMT  
		Size: 9.2 MB (9242575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fffded0152124473eb3f6771b9586bb4209cb488040de5988853b0c729cf7d`  
		Last Modified: Fri, 14 Nov 2025 02:00:08 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d816df4d772f8f751c1f729df5148274d14686749691a165ff41eec29f2866e`  
		Last Modified: Fri, 14 Nov 2025 02:00:07 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian` - unknown; unknown

```console
$ docker pull maven@sha256:4ec7bff88fda8e3124fbab6d3d2f55795871cd20d88d03492710e9e1e733f91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ab67d61d3fd4e403d3354912d160e034b929c93364433c77814536f72bd230`

```dockerfile
```

-	Layers:
	-	`sha256:391d9f2a3c7b5931869cef5deec7a2cb06ea5a8915ba9d424d7c72902ca904b9`  
		Last Modified: Fri, 14 Nov 2025 03:29:18 GMT  
		Size: 3.0 MB (2964793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14a9005d8cdf047adca4e2c1b6b42d6efcc2c3f6c80f0f72ae45aab1d16f7226`  
		Last Modified: Fri, 14 Nov 2025 03:29:19 GMT  
		Size: 19.4 KB (19381 bytes)  
		MIME: application/vnd.in-toto+json
