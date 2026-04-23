## `maven:3-amazoncorretto-11-alpine`

```console
$ docker pull maven@sha256:39e2aa6b0799d8304a3c47e21e254afad1927c1b7a7f2f338caded78bfdfaf95
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-alpine` - linux; amd64

```console
$ docker pull maven@sha256:5dfff213ebe489d2947f46f1f2fa35eb083bf4bc777d09bb4d4fff2ab1f2dc8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159284910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c047384859f94700cd3110822cf282aef4dd88002908ef5cbc69d900cb095c4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:33:41 GMT
ARG version=11.0.31.11.1
# Wed, 22 Apr 2026 21:33:41 GMT
# ARGS: version=11.0.31.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:33:41 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:33:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:33:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 22 Apr 2026 22:14:39 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 22 Apr 2026 22:14:39 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 22 Apr 2026 22:14:39 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 22 Apr 2026 22:14:39 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 22 Apr 2026 22:14:39 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 22 Apr 2026 22:14:39 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 22 Apr 2026 22:14:39 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 22 Apr 2026 22:14:39 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 22 Apr 2026 22:14:39 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 22 Apr 2026 22:14:39 GMT
ARG USER_HOME_DIR=/root
# Wed, 22 Apr 2026 22:14:39 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 22 Apr 2026 22:14:39 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 22 Apr 2026 22:14:39 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99393aeb4996979729334549f2441c549bce4b33ff304c9e42cdc66c6103a224`  
		Last Modified: Wed, 22 Apr 2026 21:33:59 GMT  
		Size: 143.7 MB (143687228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe688d918e61430d48f7777ecad50b6aac5b4caa921c4c95926227fdfd4b4654`  
		Last Modified: Wed, 22 Apr 2026 22:14:47 GMT  
		Size: 2.4 MB (2420264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04283e52c003461fb5d130bfd89c34a4935ddadc93cd60d736b7c3323de9724`  
		Last Modified: Wed, 22 Apr 2026 22:14:47 GMT  
		Size: 9.3 MB (9312220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f240923877567e0ebd1a69c385b0c2736de29904b6e69009540a32ac779e8ed`  
		Last Modified: Wed, 22 Apr 2026 22:14:47 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69dfa9b7cb3d992ab2f66e9ef66421f1702df66a5e163ff9f8da172d6f47b217`  
		Last Modified: Wed, 22 Apr 2026 22:14:46 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:cd3f8022ddefceac97bd184c99f2ef268ab8783b6f3325d15cca07305ce3f8ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **748.1 KB (748059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad045a78ccbd9e4838a6596bb30f1d0c31ba34b545936a898208d180239ecd7a`

```dockerfile
```

-	Layers:
	-	`sha256:16eebfeebcfe307a228b26393712d650e6ff1199ef593c02639d6d41d24db79a`  
		Last Modified: Wed, 22 Apr 2026 22:14:47 GMT  
		Size: 733.5 KB (733534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd8e11a596e6d3bb576f2bcae820b6ba4d5bc6256d691c569807e09d628ee419`  
		Last Modified: Wed, 22 Apr 2026 22:14:46 GMT  
		Size: 14.5 KB (14525 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:c52255bdbfa14af92fc5fb35f44c884de092f64b5d23dd1d04b9cf66f2edabf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.9 MB (157936797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6079b515485ff13bee790dd68d19ca482034a226aa6c4e2f8bc4294ff064922a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:33:42 GMT
ARG version=11.0.31.11.1
# Wed, 22 Apr 2026 21:33:42 GMT
# ARGS: version=11.0.31.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:33:42 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:33:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:33:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 22 Apr 2026 22:14:33 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 22 Apr 2026 22:14:33 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 22 Apr 2026 22:14:33 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 22 Apr 2026 22:14:33 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 22 Apr 2026 22:14:33 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 22 Apr 2026 22:14:33 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 22 Apr 2026 22:14:33 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 22 Apr 2026 22:14:33 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 22 Apr 2026 22:14:33 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 22 Apr 2026 22:14:33 GMT
ARG USER_HOME_DIR=/root
# Wed, 22 Apr 2026 22:14:33 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 22 Apr 2026 22:14:33 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 22 Apr 2026 22:14:33 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4481cbdadb4172f48c8936373d9b5437fcb703976a755acfcc8875d8ffdafced`  
		Last Modified: Wed, 22 Apr 2026 21:33:59 GMT  
		Size: 142.0 MB (141962305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848646517822c9f365ab2c9e345fc7775b9360f942dc5f525092728b8c6421b2`  
		Last Modified: Wed, 22 Apr 2026 22:14:41 GMT  
		Size: 2.5 MB (2461351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e66c012addfda8c5fb3bed422b6318c5b4a308ea93e4e8b31d40734281e5b7`  
		Last Modified: Wed, 22 Apr 2026 22:14:41 GMT  
		Size: 9.3 MB (9312261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720901057218c17b30b51eaf630b74b2882a3b17205f37b20a0165d753656111`  
		Last Modified: Wed, 22 Apr 2026 22:14:41 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0738d1982eb9174bc753190fd48e9eba1f22e67c5c48076f336d6fe579d6fb84`  
		Last Modified: Wed, 22 Apr 2026 22:14:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:d2b45ea343b17b4e6b98646306017996258c3338dc8025aae666b20731b192f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **747.6 KB (747587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d45404ccc74fb5f84b4ed55fccc40c2f71d25757c149b4a68c52e397e17d38`

```dockerfile
```

-	Layers:
	-	`sha256:e10d7b5976e22b288c73d3324fba34c258d697785e2444fef2b89eb6d34487f0`  
		Last Modified: Wed, 22 Apr 2026 22:14:41 GMT  
		Size: 732.9 KB (732928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eb6412e4bf809bad1e81aa1d2dcdc6c8e8bb8c75abcb941ca54a91334f9100b`  
		Last Modified: Wed, 22 Apr 2026 22:14:41 GMT  
		Size: 14.7 KB (14659 bytes)  
		MIME: application/vnd.in-toto+json
