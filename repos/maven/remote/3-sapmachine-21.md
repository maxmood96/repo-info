## `maven:3-sapmachine-21`

```console
$ docker pull maven@sha256:4206039ad5cb4c10d527bf2a65d1c70c6970a0cae5acc2985e386cc5de4d39af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-sapmachine-21` - linux; amd64

```console
$ docker pull maven@sha256:0391c5d5c57b96178901418e2eb22db1d8437529a74223df9aec67e1a0c7e564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.0 MB (281010226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81aae4381aa9cd994f6a57a379a9add6583b310d2470f851158071e33df51a3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:16:50 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:16:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 15 Apr 2026 20:16:50 GMT
CMD ["jshell"]
# Wed, 15 Apr 2026 22:53:13 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:53:13 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 15 Apr 2026 22:53:13 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 22:53:13 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 22:53:13 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 15 Apr 2026 22:53:13 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Apr 2026 22:53:13 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 15 Apr 2026 22:53:13 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 22:53:13 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 15 Apr 2026 22:53:14 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 15 Apr 2026 22:53:14 GMT
ARG MAVEN_VERSION=3.9.14
# Wed, 15 Apr 2026 22:53:14 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Apr 2026 22:53:14 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Apr 2026 22:53:14 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Apr 2026 22:53:14 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07edda880038f14faf7bdf8c083af072ba39fbfe944ed22b60b243c755aadca`  
		Last Modified: Wed, 15 Apr 2026 20:17:14 GMT  
		Size: 216.5 MB (216494920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73f9379ffe85938ccef15dd5c8894a08f06010ac7a9c2a61c38b720fb941d3a`  
		Last Modified: Wed, 15 Apr 2026 22:53:27 GMT  
		Size: 25.5 MB (25470096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b099bc14f3707bea054181811236c4cc040694ed6e0a4337078e94170db0cf83`  
		Last Modified: Wed, 15 Apr 2026 22:53:27 GMT  
		Size: 9.3 MB (9311195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179b7de39135be9587e211595a00ebd201c2f74889bde691682c81707b25e1d7`  
		Last Modified: Wed, 15 Apr 2026 22:53:26 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8390888fafaec26de1d19d85abc6e7b011d3e1bda1095fb382f6a9a93311979c`  
		Last Modified: Wed, 15 Apr 2026 22:53:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-21` - unknown; unknown

```console
$ docker pull maven@sha256:05bea3b99119f4a87e19fc8e26befa24086bc1adf0fdb627bae30ac7d9bac45e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4338915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e0b2e779c134597d62a501a9526fb6d9f7e347a0ba68d646e08a8029ebfa64`

```dockerfile
```

-	Layers:
	-	`sha256:7275ae36dca47642b5f6610eec5a4556c6ed121983f41e673c1acc77a4685e00`  
		Last Modified: Wed, 15 Apr 2026 22:53:27 GMT  
		Size: 4.3 MB (4322412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdf5167cd08f00bbc4a0f09c39cc58310d23a6af8ad6bcb93aac6e72b0b3be62`  
		Last Modified: Wed, 15 Apr 2026 22:53:27 GMT  
		Size: 16.5 KB (16503 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:b758308bb7d28b72a45e23f48d889301ed5d0470e61c86dd97472089d24229ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278478888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91be82b1f196ec49519d0969fbb14dc350e5b00ad5269bca4183db519562868`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:08:59 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:08:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 15 Apr 2026 21:08:59 GMT
CMD ["jshell"]
# Wed, 15 Apr 2026 23:19:31 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:19:31 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 15 Apr 2026 23:19:31 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 23:19:31 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 23:19:31 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 15 Apr 2026 23:19:31 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Apr 2026 23:19:31 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 15 Apr 2026 23:19:31 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 23:19:31 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 15 Apr 2026 23:19:31 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 15 Apr 2026 23:19:31 GMT
ARG MAVEN_VERSION=3.9.14
# Wed, 15 Apr 2026 23:19:31 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Apr 2026 23:19:31 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Apr 2026 23:19:31 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Apr 2026 23:19:31 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1f01acc0dd797cbe5018cfd7b43708d4cc44f7d615696571ae019ac02a084d`  
		Last Modified: Wed, 15 Apr 2026 21:09:24 GMT  
		Size: 214.8 MB (214757430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20c82928be1961b67af35eba965e6c277c561e270f05325a59c5eede6470159`  
		Last Modified: Wed, 15 Apr 2026 23:19:45 GMT  
		Size: 25.5 MB (25533438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66aa0c111a1fc877d49312172747e532826beadd8c557bab04ebc70678773a17`  
		Last Modified: Wed, 15 Apr 2026 23:19:44 GMT  
		Size: 9.3 MB (9311195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e7075a0e5274b6ce94531f02cef9e3ac5759a6b0529d3574f39fc8459711cc`  
		Last Modified: Wed, 15 Apr 2026 23:19:44 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e038c678b41c202a7fad83bf23951a3d979262a364b5ded8f315b33ffb767115`  
		Last Modified: Wed, 15 Apr 2026 23:19:44 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-21` - unknown; unknown

```console
$ docker pull maven@sha256:9f9a141a713d94fa502053e39d23c1cda40f8893eaff225b639b83d6d0648f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4345570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbcf99ac180250ed438779881a9c1d2ae7f5bb63efb9f1530608dfdb8e6f2ce7`

```dockerfile
```

-	Layers:
	-	`sha256:59d37732dace674492fb30d545993aef7f5e22b0a389feed8b139edb6cad2653`  
		Last Modified: Wed, 15 Apr 2026 23:19:44 GMT  
		Size: 4.3 MB (4328934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3ecab4b1ca728ed0ee5f197eeea6229406a59cffbf70a2e505be68e4ea51d78`  
		Last Modified: Wed, 15 Apr 2026 23:19:44 GMT  
		Size: 16.6 KB (16636 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-21` - linux; ppc64le

```console
$ docker pull maven@sha256:5196c0b3793f4a0327750fc3f7939f168f4281c996093b3355b4a096584486bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.2 MB (291171953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11915b06812f27835c62064353e28d00f4b7c6d7329b05ada7b1fd321ad8f745`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 23:32:43 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:32:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 15 Apr 2026 23:32:43 GMT
CMD ["jshell"]
# Thu, 16 Apr 2026 05:46:00 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Apr 2026 05:46:01 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 16 Apr 2026 05:46:01 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 16 Apr 2026 05:46:01 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 16 Apr 2026 05:46:01 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 16 Apr 2026 05:46:01 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 16 Apr 2026 05:46:01 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 16 Apr 2026 05:46:01 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 16 Apr 2026 05:46:02 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 16 Apr 2026 05:46:02 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 16 Apr 2026 05:46:02 GMT
ARG MAVEN_VERSION=3.9.14
# Thu, 16 Apr 2026 05:46:02 GMT
ARG USER_HOME_DIR=/root
# Thu, 16 Apr 2026 05:46:02 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 16 Apr 2026 05:46:02 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 16 Apr 2026 05:46:02 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97c02826fb95077af5a8efe575b06d8b01b0a456d6b55eceb311bf0f7bd2fee`  
		Last Modified: Wed, 15 Apr 2026 23:33:24 GMT  
		Size: 217.5 MB (217549863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204fdb8261bb10a8c1af673d13b6aaec8a6661368d8036dac82c8ee532ddfe8d`  
		Last Modified: Thu, 16 Apr 2026 05:46:35 GMT  
		Size: 30.0 MB (29995685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bfade127e88ab4a1d5cdcaec4d490fd3e5c7b404c87eb416da724277a338046`  
		Last Modified: Thu, 16 Apr 2026 05:46:34 GMT  
		Size: 9.3 MB (9311190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e63de20dc6041ae85fcde5e91e689f3da51cf0a9cdc72fe53b93a339cf2b65`  
		Last Modified: Thu, 16 Apr 2026 05:46:33 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527653ebf6344812bd13d8fd1cd67098cfcd574cec793e8e99f0e5514a716dc3`  
		Last Modified: Thu, 16 Apr 2026 05:46:33 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-21` - unknown; unknown

```console
$ docker pull maven@sha256:230416f817e8104a3752dd0ab619491f9c5269671cf449954964d4bca72ede21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4339394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4324cd3eabdda80535bdd206eb951e8e94762b4fb256d3b5ee355f2672bdee18`

```dockerfile
```

-	Layers:
	-	`sha256:2d26f650d1b85812aa5937367b819e08f14fa6575655e81bf89ac2988696b864`  
		Last Modified: Thu, 16 Apr 2026 05:46:34 GMT  
		Size: 4.3 MB (4322841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eee439370db0b18c25078dfb0b243a5e740b2b8263c5a16ea9440f6abd4fb14a`  
		Last Modified: Thu, 16 Apr 2026 05:46:33 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json
