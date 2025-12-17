## `maven:3-amazoncorretto-8-debian`

```console
$ docker pull maven@sha256:975ba60cc739b9f8b9a80211027a2d52f82b0cb4ac99323936cc8f556c30384b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-debian` - linux; amd64

```console
$ docker pull maven@sha256:feade84bef9829ece799a065829cf20596a20db173eb6ef218979a7def03ceae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164681925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6647624c505d3fb56ee7c46fe433d9a307ab32a131aae88bb7d9ca0acf9265d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 20:09:27 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 20:09:27 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:09:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Wed, 17 Dec 2025 20:09:27 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 17 Dec 2025 20:09:27 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:09:27 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:09:27 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 17 Dec 2025 20:09:27 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 17 Dec 2025 20:09:27 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 17 Dec 2025 20:09:27 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 17 Dec 2025 20:09:27 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 17 Dec 2025 20:09:27 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 17 Dec 2025 20:09:27 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 17 Dec 2025 20:09:27 GMT
ARG USER_HOME_DIR=/root
# Wed, 17 Dec 2025 20:09:27 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 17 Dec 2025 20:09:27 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 17 Dec 2025 20:09:27 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a57186a5ccd7c9e372fce7df1697fb65abdb41d8d4f21a18f0fb0750a612b6`  
		Last Modified: Wed, 17 Dec 2025 20:10:08 GMT  
		Size: 125.6 MB (125592148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d5de8e22d16764bb2c9d511e34587ca1045798238d5a981e1e6b04cc8cdad6`  
		Last Modified: Wed, 17 Dec 2025 20:09:51 GMT  
		Size: 9.3 MB (9312243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f7d5cfd05a858570762136684c45c129637c22e84dab9dbb55775798eeb119`  
		Last Modified: Wed, 17 Dec 2025 20:09:49 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53dcebc718d433ee1c0a303bd6021cf6e38f49d437e2736f3acb9ea019622c30`  
		Last Modified: Wed, 17 Dec 2025 20:09:49 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian` - unknown; unknown

```console
$ docker pull maven@sha256:c40a78854d0473db61acb2b8d06c627c8741c2b07244f3d0b2e0d8216b462854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3001181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047c7e8af444b6c6750f563359019069bea791f5434caa777a77aee5003ee114`

```dockerfile
```

-	Layers:
	-	`sha256:ea3260025a6752ea6d3984ab56460d3bd01d92809124b0b4bffe13937b5f1c6a`  
		Last Modified: Wed, 17 Dec 2025 21:30:36 GMT  
		Size: 3.0 MB (2981969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a18c38d8d106f282df5909660c56adbea71d3a19ac6da4befe330477bbd41a5d`  
		Last Modified: Wed, 17 Dec 2025 21:30:37 GMT  
		Size: 19.2 KB (19212 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:0168b921883143021c9325c9ce9ed8e1350a770e427f179383527a9d2f5d8ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (149018909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19bfbbb522ffa7d391de875c72aa0fba95323cd20074cb48da1117e46d9e1ecd`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 20:09:33 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo 'a4f2307774f79869ec41a667228c563fb086a267ac101ba44cc14fa515595c54 *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Dec 2025 20:09:34 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:09:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Wed, 17 Dec 2025 20:09:34 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 17 Dec 2025 20:09:34 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:09:34 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:09:34 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 17 Dec 2025 20:09:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 17 Dec 2025 20:09:34 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 17 Dec 2025 20:09:34 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 17 Dec 2025 20:09:34 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 17 Dec 2025 20:09:34 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 17 Dec 2025 20:09:34 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 17 Dec 2025 20:09:34 GMT
ARG USER_HOME_DIR=/root
# Wed, 17 Dec 2025 20:09:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 17 Dec 2025 20:09:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 17 Dec 2025 20:09:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca6cbc37c8826a01faf990f8f78165053b66d00b8f4e133c2a61a8f7389e873`  
		Last Modified: Wed, 17 Dec 2025 20:10:06 GMT  
		Size: 109.6 MB (109566995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c400776f2343200257a468e5ab4604282d9b73d9dcb90b2c14312e4fcb0cd9`  
		Last Modified: Wed, 17 Dec 2025 20:09:55 GMT  
		Size: 9.3 MB (9312248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7195bb62f45f82759c348899a81a4201a2745b15ec56fe7165a61c29405369`  
		Last Modified: Wed, 17 Dec 2025 20:10:06 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9963046954ddb14367b0d0d6105b6e62adbfef74b7595552742f86d05108b2`  
		Last Modified: Wed, 17 Dec 2025 20:09:55 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian` - unknown; unknown

```console
$ docker pull maven@sha256:f4ab90cd980d676e7527d7220f210bdc150f488b72352f4327469ee5a7b4c68d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a79a0249387cbca85e321d191a882d47cdfe5fe2209e9edf48b7ac315fd5b318`

```dockerfile
```

-	Layers:
	-	`sha256:ddb2ae47abc1541681657edc87b8db384d2831cbff42f33e373cea061244c6be`  
		Last Modified: Wed, 17 Dec 2025 21:30:42 GMT  
		Size: 3.0 MB (2964790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54f3565cb904d17e4feae04a6bde264dd5e5600eb0ea99fdf15e69788b083998`  
		Last Modified: Wed, 17 Dec 2025 21:30:43 GMT  
		Size: 19.4 KB (19381 bytes)  
		MIME: application/vnd.in-toto+json
