## `maven:3-amazoncorretto-17-debian`

```console
$ docker pull maven@sha256:ae2cbc713caf81845a708bd191de1b6bcc32e33a3fc28eb6e36ee0a72cf88b37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-debian` - linux; amd64

```console
$ docker pull maven@sha256:0cf34bd5d77197d26b4eb67466199114371f5da00d6bb0efa02c7fd6bd91629e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243574980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1a742aa83f007422c38c2d5441fedac6690f8a9b523d01e1ebb08125505341`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 21 Apr 2026 18:12:06 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 18:12:07 GMT
ENV LANG=C.UTF-8
# Tue, 21 Apr 2026 18:12:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 21 Apr 2026 18:12:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 18:12:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:12:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:12:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 18:12:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 18:12:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 18:12:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 18:12:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 18:12:07 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 18:12:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 18:12:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 18:12:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1859b1c9282785b10569e023a4874bf2a2047322d8621bf6754a18520bbf21bd`  
		Last Modified: Tue, 21 Apr 2026 18:12:31 GMT  
		Size: 204.5 MB (204486138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0741979cd5f85e06cdc6423e392744576f440cdf27e1c7eac1263ef779d886a4`  
		Last Modified: Tue, 21 Apr 2026 18:12:26 GMT  
		Size: 9.3 MB (9312197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a57493df5dc55dd48c98726cc732fddd34e7df2db0ac4e6dc5ab13918f4b84`  
		Last Modified: Tue, 21 Apr 2026 18:12:25 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6548599cea807b595812ea5c0dabba9b150b18b5e230275edf1d820764a020`  
		Last Modified: Tue, 21 Apr 2026 18:12:25 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian` - unknown; unknown

```console
$ docker pull maven@sha256:78e81f6736ec6b744ef4068dd5f7454932fc0bbd4a5a7cd7992c250cad941b71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3121612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418c9c9fea0bbabe6c1e4d480c6b3d3189cfc0865394842fa0b57b0d24527743`

```dockerfile
```

-	Layers:
	-	`sha256:f8799a4e4b9ba24ba68698addbfd51b0f84c9815cd15239a1e5406a70c59fbf2`  
		Last Modified: Tue, 21 Apr 2026 18:12:25 GMT  
		Size: 3.1 MB (3104087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0e23e8ff934fd362c116a605d72d4f83cf69fb4f16e86eb97afdcc27358cda0`  
		Last Modified: Tue, 21 Apr 2026 18:12:25 GMT  
		Size: 17.5 KB (17525 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:20d100123ab4f48d8326e5603e9578e7d86caba1ef1c0f678eeeb41a86f9c704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.8 MB (239762058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b966673ba0283dbf27e5cc8b8d2fe6269afc7549ab1fc8a8ac8491f7f760a71f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:25:57 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:25:57 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 02:25:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 22 Apr 2026 02:25:57 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 22 Apr 2026 02:25:57 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 22 Apr 2026 02:25:57 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 22 Apr 2026 02:25:57 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 22 Apr 2026 02:25:57 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 22 Apr 2026 02:25:57 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 22 Apr 2026 02:25:57 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 22 Apr 2026 02:25:57 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 22 Apr 2026 02:25:57 GMT
ARG USER_HOME_DIR=/root
# Wed, 22 Apr 2026 02:25:57 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 22 Apr 2026 02:25:57 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 22 Apr 2026 02:25:57 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b154981772684a73ff098770ae715308752c9b3b0d5ffa19e4afee52352357`  
		Last Modified: Wed, 22 Apr 2026 02:26:25 GMT  
		Size: 200.3 MB (200305196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cd57c9d6709c21277ac0196822145a20211865879571c3354ca4ec74212d22`  
		Last Modified: Wed, 22 Apr 2026 02:26:18 GMT  
		Size: 9.3 MB (9312253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1ec2414dfdecdb3e8a80a2e7aee7cbeda19e58e0144ba8de0067f39bb439da`  
		Last Modified: Wed, 22 Apr 2026 02:26:17 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b062e7fae285f4cb5624eb1a60501dfbc97bd6e7c393d1799f0dcc19cdcfcb6`  
		Last Modified: Wed, 22 Apr 2026 02:26:17 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian` - unknown; unknown

```console
$ docker pull maven@sha256:014d9ea7d29cd0f65afa245fa74810a36e3f53d79e25090ab2707a309d6688d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b8fda22486154e7f763ea6ddf2abb92167ab9ceb8ae041faa4d91d0b4e93f8`

```dockerfile
```

-	Layers:
	-	`sha256:3a0a1c3f78cb8e4c98c6905ba3f7de4e2999ca0592f35a50a02c601e6df72ee3`  
		Last Modified: Wed, 22 Apr 2026 02:26:17 GMT  
		Size: 3.1 MB (3104396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ae625f8915d59a73a3b8e8fb21b2b1efee0aae73a8f97c8e53ffaf27f62032e`  
		Last Modified: Wed, 22 Apr 2026 02:26:17 GMT  
		Size: 17.7 KB (17693 bytes)  
		MIME: application/vnd.in-toto+json
