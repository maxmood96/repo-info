## `maven:3-amazoncorretto-8-debian-bookworm`

```console
$ docker pull maven@sha256:a4d57f313941522783eb05038eb2720f2d962407bf6419736e12f6dbb8db761c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-debian-bookworm` - linux; amd64

```console
$ docker pull maven@sha256:a981e44f5da7046f6aa59fdf750d93497bd2018a823fbdd896b2e75b5d1303f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163596876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae277089d63272b292ff33fe41feb2fececd9865353976382edc78f480fc33e9`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Sat, 25 Jan 2025 20:08:38 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '5fdaed0a262b975776b1d5c0170d2e86b1be1e98b27ef97114b04ec9ac7f011d *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 25 Jan 2025 20:08:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
ARG MAVEN_VERSION=3.9.9
# Sat, 25 Jan 2025 20:08:38 GMT
ARG USER_HOME_DIR=/root
# Sat, 25 Jan 2025 20:08:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 25 Jan 2025 20:08:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 25 Jan 2025 20:08:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813195c55d6b94e9c26c77f3777948abaf8836e74c0a8e71046d6cb637136a3b`  
		Last Modified: Fri, 31 Jan 2025 03:13:39 GMT  
		Size: 126.2 MB (126212983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b28224b33e3959d4966922bb0263eb496b2d253342775094e47a0f2c8df74a`  
		Last Modified: Fri, 31 Jan 2025 03:13:37 GMT  
		Size: 9.2 MB (9170440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9474f518c0a84dd04d6d29da9df0fb62bc49bea74845f3c3db7ff680d599b9f3`  
		Last Modified: Fri, 31 Jan 2025 03:13:37 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da983330ed8cefe4755092adcf081647be19c098ca0e85250b0033489d2dce43`  
		Last Modified: Fri, 31 Jan 2025 03:13:37 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian-bookworm` - unknown; unknown

```console
$ docker pull maven@sha256:38c2eafa1297f11f9072d11156f1b3cef9e1012ac362dc024a04875b90cd4f0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2893028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe5098817216c1881c2149ae261491781b353d7ce3ba03446505e8073b2e16e`

```dockerfile
```

-	Layers:
	-	`sha256:2a5422ffdfa68d3af9c061dfbbfa50693a9028a25d539b55018579ed8f2d51ca`  
		Last Modified: Fri, 31 Jan 2025 03:13:37 GMT  
		Size: 2.9 MB (2873803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0f668bb8c99a2558548152fdd3e2e24ab4f78672498bd99627afd751722268`  
		Last Modified: Fri, 31 Jan 2025 03:13:37 GMT  
		Size: 19.2 KB (19225 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-debian-bookworm` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:8ad9f71c2792540c24d28d439a1efcbe7943de8475d4f3251a122418ae13304b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.2 MB (147206596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b481010c4e1557120265bc8f2fcc949816d93d758b880ff50b908b5d097efd`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Sat, 25 Jan 2025 20:08:38 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '5fdaed0a262b975776b1d5c0170d2e86b1be1e98b27ef97114b04ec9ac7f011d *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-1.8.0-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 25 Jan 2025 20:08:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 25 Jan 2025 20:08:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 25 Jan 2025 20:08:38 GMT
ARG MAVEN_VERSION=3.9.9
# Sat, 25 Jan 2025 20:08:38 GMT
ARG USER_HOME_DIR=/root
# Sat, 25 Jan 2025 20:08:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 25 Jan 2025 20:08:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 25 Jan 2025 20:08:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e552bc6344f9c0296cc9fcdee38a6b8c69ef74ea312118cfc97018abfe823497`  
		Last Modified: Mon, 27 Jan 2025 20:24:11 GMT  
		Size: 110.0 MB (109994092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596233958681f84eb94a09e9ce5b564299127373fc718e828a8d39d3eb176801`  
		Last Modified: Mon, 27 Jan 2025 20:24:08 GMT  
		Size: 9.2 MB (9170437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d86b2b6e8b4c20ac94a56f0280236236951fdfbc64b837c8f24764eecd1484`  
		Last Modified: Mon, 27 Jan 2025 20:24:07 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd71a04439e9a4b393e58b6897954544cdfb1ecf1f01a23300159fb1d62e548`  
		Last Modified: Mon, 27 Jan 2025 20:24:08 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-debian-bookworm` - unknown; unknown

```console
$ docker pull maven@sha256:032d3dffba9fc2fe889b72e2cd7d2f68561a9f54430bf3dbf3cbe6362ba7aa4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2876015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e15b8cfc4cf66f455ac49048fee6711926ac317e29c71fb7d15b4f5be994d558`

```dockerfile
```

-	Layers:
	-	`sha256:0cc1486df1e9867df590b3b3eb2a174bb1fbb6f9b0143e49cbf79aac20cb2854`  
		Last Modified: Fri, 31 Jan 2025 06:44:57 GMT  
		Size: 2.9 MB (2856621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:413b98b27d2ad568fe9742a65df432ce3512946e6314732dc47b00d78e489c58`  
		Last Modified: Fri, 31 Jan 2025 06:44:56 GMT  
		Size: 19.4 KB (19394 bytes)  
		MIME: application/vnd.in-toto+json
