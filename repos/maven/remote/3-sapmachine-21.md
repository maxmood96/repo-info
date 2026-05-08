## `maven:3-sapmachine-21`

```console
$ docker pull maven@sha256:888f950ea12cebbc50eec7225574789a7161ac9f4b39ee889c589f7e271203ea
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
$ docker pull maven@sha256:cc0a5daf739e17bdb5f57b2642b50cced187b3c250836a06cd604997e99bc40b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.2 MB (281214913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffdafd808f71d100a6e147fdd0588dac5134dccc1ebe6f3d1680a543e284617`
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
# Tue, 21 Apr 2026 23:04:33 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.11 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:04:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Apr 2026 23:04:33 GMT
CMD ["jshell"]
# Tue, 21 Apr 2026 23:15:06 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:15:06 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 23:15:06 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 23:15:06 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 23:15:06 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 23:15:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 23:15:06 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 23:15:06 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 23:15:06 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 23:15:06 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 23:15:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 23:15:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 23:15:06 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e68cd0672d5527b4d1f51e79d5d9b22a33242ede81b09f9778fc83882ea259`  
		Last Modified: Tue, 21 Apr 2026 23:04:56 GMT  
		Size: 216.7 MB (216699386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf2aa05b2c28ce321cc0b001f4aca6315ca1c56b8208ae34dcbc6cae1070974`  
		Last Modified: Tue, 21 Apr 2026 23:15:19 GMT  
		Size: 25.5 MB (25469325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473df2000bfa83a137e46bf9a3a2ab3da60288b603a519d3475d474d2d334696`  
		Last Modified: Tue, 21 Apr 2026 23:15:19 GMT  
		Size: 9.3 MB (9312218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1dfba950292e8b236c3eabeb11a3e84cb6ac0838db99e75a7244aec8644d040`  
		Last Modified: Tue, 21 Apr 2026 23:15:18 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fcd06a3970c20e217d32d3a4e9053e3a51233d40afc9ca019d186f879481a5`  
		Last Modified: Tue, 21 Apr 2026 23:15:18 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-21` - unknown; unknown

```console
$ docker pull maven@sha256:7ee3514e73cb6b718fbc9478df828c20f34292dd9d9f8066311a070ca5616e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4337695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95311c34c9e362c73bffac422cdc25144b0fe16a156fd765a6379eb89f388b1d`

```dockerfile
```

-	Layers:
	-	`sha256:e5f50456356e94b55b107db23fcb0c0bc6d0d116b8de0842d1e03a8d3ef89f5a`  
		Last Modified: Tue, 21 Apr 2026 23:15:18 GMT  
		Size: 4.3 MB (4323030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a836497df8b5e81eff25a421bab8f7fd61b061d079f0da3ddc61cde8cb8e2002`  
		Last Modified: Tue, 21 Apr 2026 23:15:18 GMT  
		Size: 14.7 KB (14665 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:8bce825a44ee05cac08c947a73289b81c41f90c05658020880a085a643925b10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.7 MB (278692155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fbfaa55a9d938f35d4bdc9e1d359a9671474a256264f8100bc32eeaf584d81`
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
# Tue, 21 Apr 2026 23:06:01 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.11 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:06:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Apr 2026 23:06:01 GMT
CMD ["jshell"]
# Fri, 08 May 2026 00:30:35 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 00:30:36 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 08 May 2026 00:30:36 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 00:30:36 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 00:30:36 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 08 May 2026 00:30:36 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 08 May 2026 00:30:36 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 08 May 2026 00:30:36 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 08 May 2026 00:30:36 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 08 May 2026 00:30:36 GMT
ARG USER_HOME_DIR=/root
# Fri, 08 May 2026 00:30:36 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 08 May 2026 00:30:36 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 08 May 2026 00:30:36 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116c8f695f5bbc3d9af2a934785ba0357feff2fbc9093b115cf8a15b38ddc84b`  
		Last Modified: Tue, 21 Apr 2026 23:06:28 GMT  
		Size: 215.0 MB (214967385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625ba834c9fd5cd69a6d642c66badedd7a0064fe82300675b4bf3b5cfd2e465e`  
		Last Modified: Fri, 08 May 2026 00:30:50 GMT  
		Size: 25.5 MB (25535720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6f2e6f98042447c01bf9f015384eb3d29e3ec7216e1932cd0712d188caeaa3`  
		Last Modified: Fri, 08 May 2026 00:30:57 GMT  
		Size: 9.3 MB (9312259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e148f75bed0b7c9dbaac2eaa105b93f3c39e689c456a4ae3ab769b3df079e3`  
		Last Modified: Fri, 08 May 2026 00:30:49 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96fc53918daeb52bb68271d02ceb589291ee3941ab128e1ff5a82c958f66667a`  
		Last Modified: Fri, 08 May 2026 00:30:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-21` - unknown; unknown

```console
$ docker pull maven@sha256:37b1a03db9fc1b45a15929456f6dd832dce32ea32dbf5d6b28ba325d47dfb413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4344504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a300f904c5ee44e2aa2defbd0dbd0f6c36f371d94d7b849c41c2ebe0868ed188`

```dockerfile
```

-	Layers:
	-	`sha256:ff8ca1f13ffab96d03c3a0d2da8220f68982e920305b9ee505fc9c9669bb63f8`  
		Last Modified: Fri, 08 May 2026 00:30:49 GMT  
		Size: 4.3 MB (4329552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90abb2cace9b31feb28a5231e266254cf103faecebfb64b874acd023827dca88`  
		Last Modified: Fri, 08 May 2026 00:30:49 GMT  
		Size: 15.0 KB (14952 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-21` - linux; ppc64le

```console
$ docker pull maven@sha256:34e8ba25c0f533892415b9cbd504e0918901e9aa563643a409420b24e6fe40cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.4 MB (291390267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a591c81829797f10d2918dc9464af5124a7c49a7fe09683080b7c35dabfa3460`
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
# Tue, 21 Apr 2026 23:20:57 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.11 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:20:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Apr 2026 23:20:57 GMT
CMD ["jshell"]
# Wed, 22 Apr 2026 00:20:44 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 00:20:45 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 22 Apr 2026 00:20:45 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 22 Apr 2026 00:20:45 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 22 Apr 2026 00:20:45 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 22 Apr 2026 00:20:45 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 22 Apr 2026 00:20:45 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 22 Apr 2026 00:20:45 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 22 Apr 2026 00:20:46 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 22 Apr 2026 00:20:46 GMT
ARG USER_HOME_DIR=/root
# Wed, 22 Apr 2026 00:20:46 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 22 Apr 2026 00:20:46 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 22 Apr 2026 00:20:46 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24057afa9cf35b99427158d98968c9a3ad3bf4110d2f01ca36f4eab8fe57f506`  
		Last Modified: Tue, 21 Apr 2026 23:21:47 GMT  
		Size: 217.8 MB (217766851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c5b411ad62aac76e1197d9da8ccfc32b63dfb7343c7ab843c930a422c04bd4`  
		Last Modified: Wed, 22 Apr 2026 00:21:18 GMT  
		Size: 30.0 MB (29995978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64585e1140fe1d3d360feca00fc63aa8b5f6c707f776f13e470330a490d8072c`  
		Last Modified: Wed, 22 Apr 2026 00:21:17 GMT  
		Size: 9.3 MB (9312252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3f462057ebee6292378537a32a54d5b4dbfa5f6191ce0818e987b71b8676be`  
		Last Modified: Wed, 22 Apr 2026 00:21:17 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba5e1d7c27c16e16a321c4f8753db0c1a63182ccb2cdf36ad366800c5d68465`  
		Last Modified: Wed, 22 Apr 2026 00:21:17 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-21` - unknown; unknown

```console
$ docker pull maven@sha256:8fc5d6c5c39173171430ca631552bdec48ffae43d731997bf67e1d770f4b332e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4338173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:329f2b938d4879a71132c54c876115a2580734b845e6ac6a14aa507021c11b09`

```dockerfile
```

-	Layers:
	-	`sha256:3a329c94a270a31a37537571b8b8b40a258d472c2d71047db3618ea0055fa863`  
		Last Modified: Wed, 22 Apr 2026 00:21:17 GMT  
		Size: 4.3 MB (4323459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a511e395b44a87208a4f3f41bc7769ea24013587bb4efc4953c9e7280c6ade9f`  
		Last Modified: Wed, 22 Apr 2026 00:21:17 GMT  
		Size: 14.7 KB (14714 bytes)  
		MIME: application/vnd.in-toto+json
