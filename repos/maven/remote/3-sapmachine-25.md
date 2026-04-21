## `maven:3-sapmachine-25`

```console
$ docker pull maven@sha256:af08675679f5c6e2da3eef2a5ecdde94347cfae3633caa9308d659958037b1c7
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
$ docker pull maven@sha256:6bfd873d9342d875a7813e080c8ecfb525850938b02707abcebe81a8f4f2f2bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (285969257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7291f49a1b665df67fb355ca2e2976491c092556e6eb88080003e0c7ee67735b`
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
# Tue, 21 Apr 2026 18:13:10 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 18:13:11 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 18:13:11 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:13:11 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:13:11 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 18:13:11 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 18:13:11 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 18:13:11 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 18:13:11 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 18:13:11 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 18:13:11 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 18:13:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 18:13:11 GMT
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
	-	`sha256:325045cdeb9ce85247cfdb97579bc60bca4802356d27024cf9741893afe1c9a8`  
		Last Modified: Tue, 21 Apr 2026 18:13:26 GMT  
		Size: 25.5 MB (25469842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789e39396b635e63576f952de81e130c7f3a94aeda1417d793be9dcee7b2eaed`  
		Last Modified: Tue, 21 Apr 2026 18:13:23 GMT  
		Size: 9.3 MB (9312203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e9ba627eafc4c4df45fb9ccfd8bd5aa2ba26aabb471482c9e451db53bcb84a`  
		Last Modified: Tue, 21 Apr 2026 18:13:24 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe93a3bc3cde771fba5c193d88b288962f5d072434167e9654147aa76911fd12`  
		Last Modified: Tue, 21 Apr 2026 18:13:24 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-25` - unknown; unknown

```console
$ docker pull maven@sha256:9a2e8599f3dcfc1842c585920da692c6b7c397bb78ad8cd26ec5da2f88b45d59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4326511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa91da2d8b80208cb51109a387cb66ece29848d327044f75ccfddbb6d8f4dfc`

```dockerfile
```

-	Layers:
	-	`sha256:c7c8adb6d3717a7e774159570aaa95f761c9c9ade1e57f726093b666a8d8e09e`  
		Last Modified: Tue, 21 Apr 2026 18:13:24 GMT  
		Size: 4.3 MB (4311846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5978fe6b5f36e63d7b1325a0e87987b8e0290ece7c87b8a0a3c964c16ef0a44f`  
		Last Modified: Tue, 21 Apr 2026 18:13:24 GMT  
		Size: 14.7 KB (14665 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-25` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:40a2b0c1cf58c724a04d957ce72060058fc9ee9b8e36e790318f01d191387479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (282989053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177a0789afc239f1e01eeeb4366d992cbeebc7aec6795b5f60603136aac60387`
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
# Tue, 21 Apr 2026 18:13:05 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 18:13:05 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 18:13:05 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:13:05 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:13:05 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 18:13:05 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 18:13:05 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 18:13:05 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 18:13:05 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 18:13:05 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 18:13:05 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 18:13:05 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 18:13:05 GMT
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
	-	`sha256:6d670faa9288756ccf588a21b2912cb5231dba355489959cdcf44a52e04f02a8`  
		Last Modified: Tue, 21 Apr 2026 18:13:19 GMT  
		Size: 25.5 MB (25533503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebedfff4809631b8cf2feabc33e05df8fdc2818e90fac8176e50e321ded0c25b`  
		Last Modified: Tue, 21 Apr 2026 18:13:18 GMT  
		Size: 9.3 MB (9312253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319745e8de884a4a6799a86b72b5eff62506ad666ad8c93a87dd8712b4d62949`  
		Last Modified: Tue, 21 Apr 2026 18:13:18 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204def0a51609e1c61717ded93778ae6ec06559149b9c3e990e883e11a880bec`  
		Last Modified: Tue, 21 Apr 2026 18:13:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-25` - unknown; unknown

```console
$ docker pull maven@sha256:ec27ef59b446bbe189fa6363f6caf7c2edbf63e22a18351efffd19f65af603c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4333163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9591b8cff166ef78916e27839aa764f2cd1a8ca31abe8682e9ebd1807f5abd9b`

```dockerfile
```

-	Layers:
	-	`sha256:8afa15a478dcbdd40f0f9f4a5f7ba992db22bc288c7855caf5dcef22641d5121`  
		Last Modified: Tue, 21 Apr 2026 18:13:18 GMT  
		Size: 4.3 MB (4318365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:809bdd51f1538f0e82164c9ac13ccf106ec6e28dfdc3e8718b3844f7f6364a4c`  
		Last Modified: Tue, 21 Apr 2026 18:13:18 GMT  
		Size: 14.8 KB (14798 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-25` - linux; ppc64le

```console
$ docker pull maven@sha256:4a9b615704e070993fc3a55537fbf774648f74372a2ae989926e23d7d19cdd76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.0 MB (295975307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6efaac467caa9569be0765d89760405b43b1960ab8d7727ace56c54386bb59b2`
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
# Tue, 21 Apr 2026 18:13:10 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 18:13:10 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:13:10 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:13:10 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 18:13:10 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 18:13:10 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 18:13:11 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 18:13:12 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 18:13:12 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 18:13:12 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 18:13:12 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 18:13:12 GMT
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
	-	`sha256:4aba61298b0b8abaf27500a4bf6c141833fd9223621c4dc12363d9e06595c5fd`  
		Last Modified: Tue, 21 Apr 2026 18:13:37 GMT  
		Size: 9.3 MB (9312258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544975fe4064e67d4f5131afbc5911ae515376eedd2fe21e9d616c30530a7393`  
		Last Modified: Tue, 21 Apr 2026 18:13:37 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aac50b5cd22950eb69944516b5bf450fbc9e0ebe6bc81c123b99e26c6dd9f12`  
		Last Modified: Tue, 21 Apr 2026 18:13:36 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-25` - unknown; unknown

```console
$ docker pull maven@sha256:4e3ea71753f2bfd31f55464306a41311067b658b850b38ca24ed8b82e6e3115e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4326372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:319f0687eca74eac9dadafc4177adc6710d645088ea361a76b7f32f820ab9dfd`

```dockerfile
```

-	Layers:
	-	`sha256:8816e61456941c2f447881e3a0369f252c581fb5b0ffe01c9029393f21d8234e`  
		Last Modified: Tue, 21 Apr 2026 18:13:37 GMT  
		Size: 4.3 MB (4311657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a13733b993e82c795a30b85c3a7cd02257699cae5fef66f58d4219382d36f2a`  
		Last Modified: Tue, 21 Apr 2026 18:13:36 GMT  
		Size: 14.7 KB (14715 bytes)  
		MIME: application/vnd.in-toto+json
