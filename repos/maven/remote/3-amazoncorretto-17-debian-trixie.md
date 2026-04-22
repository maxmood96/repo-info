## `maven:3-amazoncorretto-17-debian-trixie`

```console
$ docker pull maven@sha256:c3db8e35b5ee1d1c3b8274132d6dec0890c1b217123a2c00bc7edf1f3204eed9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:8e291624c92774523b312f4978e0e2f66c3d5b38cc672f04d890bb527c35fa9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240863680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfca11470cc0efc786f00567939a6f7c1a9f5392ffc4bae22b5b86944f869bbd`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:22:52 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:22:52 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 02:22:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 22 Apr 2026 02:22:52 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 22 Apr 2026 02:22:52 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 22 Apr 2026 02:22:52 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 22 Apr 2026 02:22:52 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 22 Apr 2026 02:22:52 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 22 Apr 2026 02:22:52 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 22 Apr 2026 02:22:52 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 22 Apr 2026 02:22:52 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 22 Apr 2026 02:22:52 GMT
ARG USER_HOME_DIR=/root
# Wed, 22 Apr 2026 02:22:52 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 22 Apr 2026 02:22:52 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 22 Apr 2026 02:22:52 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4aad2314eff1e9a7faeb82f90c232996f8e37a6d8089c08a2c780690c722cd`  
		Last Modified: Wed, 22 Apr 2026 02:23:14 GMT  
		Size: 201.8 MB (201770305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931357cbf9e7a2ae4f4967b026c2112e4493f985e367f361f40bade0db69564e`  
		Last Modified: Wed, 22 Apr 2026 02:23:10 GMT  
		Size: 9.3 MB (9312198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8424baaf15e415b9ebc58ecc93019b4ca0e66113bd6391a3cfd0063856c0036`  
		Last Modified: Wed, 22 Apr 2026 02:23:09 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5192ca4870ecad790201647c47068a737b08a651c3c631ada1149ffba4c4c973`  
		Last Modified: Wed, 22 Apr 2026 02:23:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:b6107c96f9e0aea6f31556972c21a1f64ff0785d29f915b69062a0efaa2c5f2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3122258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf001d3c4714ba0ceb73284f5443eb1a3df9bb16840d65997efdd558d0c9697`

```dockerfile
```

-	Layers:
	-	`sha256:afc1c0d066ddb97bdd9825f31dbe563f0c0fb58727c2bd5a84734fb8efb89a19`  
		Last Modified: Wed, 22 Apr 2026 02:23:09 GMT  
		Size: 3.1 MB (3104733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a70406d1451ac5e6718e601fba639cf9ab3f139429705f1125e7622301339fac`  
		Last Modified: Wed, 22 Apr 2026 02:23:09 GMT  
		Size: 17.5 KB (17525 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-debian-trixie` - linux; arm64 variant v8

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

### `maven:3-amazoncorretto-17-debian-trixie` - unknown; unknown

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
