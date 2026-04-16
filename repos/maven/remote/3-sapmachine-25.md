## `maven:3-sapmachine-25`

```console
$ docker pull maven@sha256:8cff64f09b6eda88b2257b304e79a9281239dd987791ae8e4963b74cd867910b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-sapmachine-25` - linux; amd64

```console
$ docker pull maven@sha256:cf026e8b4b0486cbc998d38414d428d9b8edda9fd0f55a44e614f495bb716cbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (285968570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce8c229bcb9072c37e964df171c894479ba163bbd0c266161fbfdcfbf6dde5d3`
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
# Wed, 15 Apr 2026 20:58:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:58:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 15 Apr 2026 20:58:16 GMT
CMD ["jshell"]
# Wed, 15 Apr 2026 22:53:25 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 22:53:25 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 15 Apr 2026 22:53:25 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 22:53:25 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 22:53:25 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 15 Apr 2026 22:53:25 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Apr 2026 22:53:25 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 15 Apr 2026 22:53:25 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 22:53:25 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 15 Apr 2026 22:53:25 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 15 Apr 2026 22:53:25 GMT
ARG MAVEN_VERSION=3.9.14
# Wed, 15 Apr 2026 22:53:25 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Apr 2026 22:53:25 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Apr 2026 22:53:25 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Apr 2026 22:53:25 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7261e992e549107f003743f60a1ec623fc178881e63f5e0d7dd4716cbbb2117d`  
		Last Modified: Wed, 15 Apr 2026 20:58:41 GMT  
		Size: 221.5 MB (221453230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c84f23f7057c7bbe2870bf37b81203288d83af87cb5dc042982e2554f90b2c`  
		Last Modified: Wed, 15 Apr 2026 22:53:40 GMT  
		Size: 25.5 MB (25470128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49ad014aa5b7495979697354fa20bf50c27ca8f018d30387e80cf337c54d951`  
		Last Modified: Wed, 15 Apr 2026 22:53:40 GMT  
		Size: 9.3 MB (9311195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6145dd823a0f85d7a1aa0d62a16f9ffcb5d0931d29b1770abda7f26455aa650`  
		Last Modified: Wed, 15 Apr 2026 22:53:39 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db1a37acfa288a5b98588a1838b354f788e0bd4c196fca46816b9b5fe02f921`  
		Last Modified: Wed, 15 Apr 2026 22:53:40 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-25` - unknown; unknown

```console
$ docker pull maven@sha256:6319a004d43644c3984deef75b7f5498c941f3a0b6afd5493109e4728c319eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4328347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e576004bcba0d10e8990ca0f795c4b27fce95e77343a6776354cc76d9b4b01`

```dockerfile
```

-	Layers:
	-	`sha256:c1a4fc750e9364cf1a299590c8da90245930172ce1c558473259b3399e445e9e`  
		Last Modified: Wed, 15 Apr 2026 22:53:39 GMT  
		Size: 4.3 MB (4311846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:388a9d11c8eb9a3209ef6bb30a7511fb31aaba7c4f3ee4ecd33889581b805a4c`  
		Last Modified: Wed, 15 Apr 2026 22:53:39 GMT  
		Size: 16.5 KB (16501 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-25` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:334a10108c2851262b843dc774e34851965de13fa36d6ae1757bf49b8714219e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (282987943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fa1156bdab5b0a3259121746f39a2e88af4fde0ddf3152c274d554a87102fb`
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
# Wed, 15 Apr 2026 21:07:30 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:07:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 15 Apr 2026 21:07:30 GMT
CMD ["jshell"]
# Wed, 15 Apr 2026 23:19:49 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:19:49 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 15 Apr 2026 23:19:49 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 23:19:49 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 15 Apr 2026 23:19:49 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 15 Apr 2026 23:19:49 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 15 Apr 2026 23:19:49 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 15 Apr 2026 23:19:49 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 23:19:49 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 15 Apr 2026 23:19:49 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 15 Apr 2026 23:19:49 GMT
ARG MAVEN_VERSION=3.9.14
# Wed, 15 Apr 2026 23:19:49 GMT
ARG USER_HOME_DIR=/root
# Wed, 15 Apr 2026 23:19:49 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 15 Apr 2026 23:19:49 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 15 Apr 2026 23:19:49 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8551e8c16388e78ab94c5d6f978fa6399edbcb20e0e40b0012046dd6e9617d`  
		Last Modified: Wed, 15 Apr 2026 21:07:57 GMT  
		Size: 219.3 MB (219266507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e59a4356ab1d214d5702cac94828bbfe44ce89e5cc9decd1d6ea5b7492e2c1`  
		Last Modified: Wed, 15 Apr 2026 23:20:03 GMT  
		Size: 25.5 MB (25533416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeaba15b702e9e8baaf3f083b8e2f53e817ee246e0d3d490abafb4a7aa9ab9a7`  
		Last Modified: Wed, 15 Apr 2026 23:20:02 GMT  
		Size: 9.3 MB (9311195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745f9d99cb159bcd776472c986a9f9b520e816f03212ef25d204a6532ea25e16`  
		Last Modified: Wed, 15 Apr 2026 23:20:02 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44821b210fe7e79ba479db02b6023d9f2789bf48f1584e6962bd501c4d3f2d91`  
		Last Modified: Wed, 15 Apr 2026 23:20:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-25` - unknown; unknown

```console
$ docker pull maven@sha256:0695ad262e11d1afe519782cf0d8b5e19d544b8c336a42490f444e7060904b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4335000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b72ab30ca181ac9ead75c8593505e7d71dab7eb3b50eff1d9f054594a5465f6`

```dockerfile
```

-	Layers:
	-	`sha256:7945afd545ca739555985fa9cbe7bd79df673fa37bc2ea7c7c41987a95ff542f`  
		Last Modified: Wed, 15 Apr 2026 23:20:02 GMT  
		Size: 4.3 MB (4318365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2d2a02dadfbdc59fd4da466957565a44c90709fbc87f3725871b878da3f4a88`  
		Last Modified: Wed, 15 Apr 2026 23:20:02 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-25` - linux; ppc64le

```console
$ docker pull maven@sha256:df593c90944487289c28b6268db9c2d9d195c60216e886f6e4ca32ba154320e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.0 MB (295974267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc581ee58f92c5546cf3566aba06ee8de6ba68c5a70c51032665972f982899a`
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
# Wed, 15 Apr 2026 23:26:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:26:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 15 Apr 2026 23:26:13 GMT
CMD ["jshell"]
# Thu, 16 Apr 2026 05:47:16 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Apr 2026 05:47:17 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 16 Apr 2026 05:47:17 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 16 Apr 2026 05:47:17 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 16 Apr 2026 05:47:17 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 16 Apr 2026 05:47:17 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 16 Apr 2026 05:47:17 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 16 Apr 2026 05:47:17 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 16 Apr 2026 05:47:17 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 16 Apr 2026 05:47:18 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 16 Apr 2026 05:47:18 GMT
ARG MAVEN_VERSION=3.9.14
# Thu, 16 Apr 2026 05:47:18 GMT
ARG USER_HOME_DIR=/root
# Thu, 16 Apr 2026 05:47:18 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 16 Apr 2026 05:47:18 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 16 Apr 2026 05:47:18 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f9b6b8049499a8cb46748347013393bd725969caa313978b9f1d5d15879e22`  
		Last Modified: Wed, 15 Apr 2026 23:26:53 GMT  
		Size: 222.4 MB (222352050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:353601b5ecfd3e9717c4200ac6d90573948c38c585360826246b8e2b6a3476f0`  
		Last Modified: Thu, 16 Apr 2026 05:47:52 GMT  
		Size: 30.0 MB (29995820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb21b398d7eac2348e962e35230c93024ff009b06a9f929e273b53d96062119`  
		Last Modified: Thu, 16 Apr 2026 05:47:52 GMT  
		Size: 9.3 MB (9311181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3186ee8f0df1357316338eeba7bd44e87240f2b0db00af2285bb88c30da4ae84`  
		Last Modified: Thu, 16 Apr 2026 05:47:51 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446c7ba98065de4c715f7bc2ce1883ee58a391203a910c3e770227303398de79`  
		Last Modified: Thu, 16 Apr 2026 05:47:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-25` - unknown; unknown

```console
$ docker pull maven@sha256:13ff6a5542fbb2644d53668dd7a8bbbbaae10d58d866f78c4ec5a68062c5c6e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4328209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68975363c2fe260ecdaf5e7f12c496b7e10befc799064cf400a633b2b74c32cf`

```dockerfile
```

-	Layers:
	-	`sha256:5c8321d94f0d9fd2b43191e0de5b5b3bba25faccbb6811b2d7bbe966f4973837`  
		Last Modified: Thu, 16 Apr 2026 05:47:52 GMT  
		Size: 4.3 MB (4311657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6739412a663d14acd558dbcf50cb1e98534ecc10251785b764c939eab2e88f3b`  
		Last Modified: Thu, 16 Apr 2026 05:47:51 GMT  
		Size: 16.6 KB (16552 bytes)  
		MIME: application/vnd.in-toto+json
