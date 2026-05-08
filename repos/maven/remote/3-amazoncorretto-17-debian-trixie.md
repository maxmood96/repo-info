## `maven:3-amazoncorretto-17-debian-trixie`

```console
$ docker pull maven@sha256:63b7fa36147bdffb3c4bbfa67b9a86439e59c790682b4f8106f2da4693933184
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:b0d2b127b6af0067c43e380a6a0ad547ceaac58ffa289f8abadea9e0b3aef3b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240863786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338ae8aa4f7f5b937452fd544248ed549746460666ed9161619ec29ad58cecf1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:30:50 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 00:30:50 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 00:30:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 08 May 2026 00:30:50 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 08 May 2026 00:30:50 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 00:30:50 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 00:30:50 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 08 May 2026 00:30:50 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 08 May 2026 00:30:50 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 08 May 2026 00:30:50 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 08 May 2026 00:30:50 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 08 May 2026 00:30:50 GMT
ARG USER_HOME_DIR=/root
# Fri, 08 May 2026 00:30:50 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 08 May 2026 00:30:50 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 08 May 2026 00:30:50 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd61febecdae96c5a1bdfcc7cdb1b6a8941a69a26f79ca4c7bc6ed5eab75889`  
		Last Modified: Fri, 08 May 2026 00:31:12 GMT  
		Size: 201.8 MB (201770374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f55aee7589c037ebdce03498b6dca89624c2d7c5d1a358f42e6e48af734e08`  
		Last Modified: Fri, 08 May 2026 00:31:09 GMT  
		Size: 9.3 MB (9312236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89ba41d20802c81435fe237c8e45d13560483be25ae73a97ccfe346d52165c7`  
		Last Modified: Fri, 08 May 2026 00:31:08 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29271458ce655872059b48c82ea9499738df147a8d5edc2cb4ed47e3fb0416d`  
		Last Modified: Fri, 08 May 2026 00:31:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:3e36592fafdd7346055c14e74f29ab534fdc265aeb8e35e57f08b6b18c2637aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d1bdbc7ca03fb91b4d91833d07b37a57015e220eca8d19c45898148176a08f`

```dockerfile
```

-	Layers:
	-	`sha256:6b270b908d678c3a3350d93a3bacf9294a2a53ae311b55117b8fbd9c78331ad6`  
		Last Modified: Fri, 08 May 2026 00:31:08 GMT  
		Size: 3.1 MB (3104733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f4291c8738718e49cf824514058372932796ef768fc6fbd8c97f2a4d64785a7`  
		Last Modified: Fri, 08 May 2026 00:31:08 GMT  
		Size: 17.7 KB (17679 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:ab8d0cd4ff699b95fa9db4f26616c7468046f88bd026cb63ee11af063b0e2dac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.8 MB (239762210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8d0cd6c73912468b0cbc25db332d29ea9908608ead7c23f8d5101baa26815a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Fri, 08 May 2026 00:29:35 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 00:29:35 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 00:29:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 08 May 2026 00:29:35 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 08 May 2026 00:29:35 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 00:29:35 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 00:29:35 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 08 May 2026 00:29:35 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 08 May 2026 00:29:35 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 08 May 2026 00:29:35 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 08 May 2026 00:29:36 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 08 May 2026 00:29:36 GMT
ARG USER_HOME_DIR=/root
# Fri, 08 May 2026 00:29:36 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 08 May 2026 00:29:36 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 08 May 2026 00:29:36 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fb1d68098b55e74ff65e96d06c37a58cc8d4ae01a288ea1bc7fc1c14e996a6`  
		Last Modified: Fri, 08 May 2026 00:30:05 GMT  
		Size: 200.3 MB (200305374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77efc8667a0481fb3854891ea90022981f19388d94e6d60dd7cfa7b5dc474cdf`  
		Last Modified: Fri, 08 May 2026 00:29:57 GMT  
		Size: 9.3 MB (9312227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce19b260c950a6ab6d2bab9b9e157528ab8aa141297ade16c4e2046eb4d2e49`  
		Last Modified: Fri, 08 May 2026 00:29:56 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25d940828b3497aacd23bb4a79078fbf440c6afcbcbd51a86ed09710ca682c4`  
		Last Modified: Fri, 08 May 2026 00:29:57 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:da5b81d44c089e18ab45c4b07035df303fde2302d1500917a8a4bc33e1b185a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b838e1032d882f3beb78b798c126efab12d453eee319f116ea7d96bc7d9ac4`

```dockerfile
```

-	Layers:
	-	`sha256:d1dd2b25e32c75bcca7c7931a753375b22e4f700f654d86f038acdd2a468230a`  
		Last Modified: Fri, 08 May 2026 00:29:57 GMT  
		Size: 3.1 MB (3104396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91fba1fefbcad6d932e17449e189a1643dbf39afc009ebeb82adc2fb5fd51075`  
		Last Modified: Fri, 08 May 2026 00:29:56 GMT  
		Size: 17.8 KB (17848 bytes)  
		MIME: application/vnd.in-toto+json
