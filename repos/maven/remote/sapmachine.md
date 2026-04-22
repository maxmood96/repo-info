## `maven:sapmachine`

```console
$ docker pull maven@sha256:6c5d0b444143df628f11df081934863b0062c9841343635638bd15f44fb4bd03
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:sapmachine` - linux; amd64

```console
$ docker pull maven@sha256:842577b54d7edea95a9a480d07c49e538e8aa451d7a64a3c861bf43417c6d88e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290893385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a13097d1414738f6d0e400bd575d6b02c8fa0005a86efb016e4bc5cd48a90e`
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
# Tue, 21 Apr 2026 23:02:49 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:02:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 21 Apr 2026 23:02:49 GMT
CMD ["jshell"]
# Tue, 21 Apr 2026 23:12:35 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:12:35 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 23:12:35 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 23:12:35 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 23:12:35 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 23:12:35 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 23:12:35 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 23:12:35 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 23:12:35 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 23:12:35 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 23:12:35 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 23:12:35 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 23:12:35 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bd5ba5e4229ebae4f482a5619f459b100f17fc3e353a279b4e2a920cc8f8a2`  
		Last Modified: Tue, 21 Apr 2026 23:03:14 GMT  
		Size: 226.4 MB (226377284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdc8d80ed68f761b62452452ef0e8fdd74dd48c27e2f2630b3c5583a24f3840`  
		Last Modified: Tue, 21 Apr 2026 23:12:48 GMT  
		Size: 25.5 MB (25469912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74f617f0ae1180eb3a8782faffda0bc31239f8d8a380b437a2d1f81fdf65f2f`  
		Last Modified: Tue, 21 Apr 2026 23:12:47 GMT  
		Size: 9.3 MB (9312204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb128cff7f660f196e5828c016056b372ecc90a1a60c3c9821d62a5f8931b108`  
		Last Modified: Tue, 21 Apr 2026 23:12:47 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6989803d98112f5efc9e895599432436c9535a6ff8c3fd62d14ab86d88afa117`  
		Last Modified: Tue, 21 Apr 2026 23:12:47 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:0fbcfd1a948b285ab9984903a91e42061175bfb453eb77cb83ff2dfd114c5a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28e57a03623bf96958f2bfc9b5b76fa81d6fc77f4787d2c6360734d3fdcc568`

```dockerfile
```

-	Layers:
	-	`sha256:7a4f6a775ec0b62ef1f02b56c1769907e7c2846ebd162afaec62868c28935fb0`  
		Last Modified: Tue, 21 Apr 2026 23:12:47 GMT  
		Size: 4.3 MB (4311189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69756504e98bde77960e21498b205ae02ef500b11011fd41020fee2c1698d902`  
		Last Modified: Tue, 21 Apr 2026 23:12:47 GMT  
		Size: 15.9 KB (15907 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:sapmachine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:77e48aa9110fb8b92c53286291c89af3214c94f45a08295b44757ddc32d648da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.0 MB (287968771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76250d1fb584e2bdc45bcd526999a8252482ff86b4ee79ac76cfd5e55b10a97`
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
# Tue, 21 Apr 2026 23:04:54 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:04:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 21 Apr 2026 23:04:54 GMT
CMD ["jshell"]
# Tue, 21 Apr 2026 23:14:12 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:14:12 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 23:14:12 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 23:14:12 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 23:14:12 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 23:14:12 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 23:14:12 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 23:14:12 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 23:14:12 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 23:14:12 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 23:14:12 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 23:14:12 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 23:14:12 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4613ade7e3c3f607887e589b004a1d8c1f4273d12de89cf733d2eb506beef91`  
		Last Modified: Tue, 21 Apr 2026 23:05:20 GMT  
		Size: 224.2 MB (224246332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ebcd4f340d3a86988114b2685aa192f2b74152c2a6a1446de77c11e8dab7f1`  
		Last Modified: Tue, 21 Apr 2026 23:14:26 GMT  
		Size: 25.5 MB (25533387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a980062397b9246f0f1c4d38fb07550589362189b1d6c0a4f4ed806b4194726a`  
		Last Modified: Tue, 21 Apr 2026 23:14:26 GMT  
		Size: 9.3 MB (9312259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc32cc4075482af74578fd3f3dcc8cdaf7efd6b1997a4c4659f0d660485b0cc`  
		Last Modified: Tue, 21 Apr 2026 23:14:25 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ecc560b0aa642bb8bf3e68f6196b81210df99f5605e81ec17d9af6539a4e2d`  
		Last Modified: Tue, 21 Apr 2026 23:14:25 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:81f2b6914c248cd98bd4464f79bb2ab14016bc70bc792fb2004500c182a21206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4333843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9901456478e2fa8c9fa0a6e385793ce55c441feea27cc4039019b72459c8461`

```dockerfile
```

-	Layers:
	-	`sha256:c14d9b13a30f4593ed8df2dffea9e658dbc14d5e4d198c2d241f23157197bfc9`  
		Last Modified: Tue, 21 Apr 2026 23:14:26 GMT  
		Size: 4.3 MB (4317756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27cbe492374bffe1863896025f0656e111d43f93278b7f5ccb505244f9477376`  
		Last Modified: Tue, 21 Apr 2026 23:14:25 GMT  
		Size: 16.1 KB (16087 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:sapmachine` - linux; ppc64le

```console
$ docker pull maven@sha256:4955ccd80f61bc53aa4a5569b5c8f16e78d425554366cd07c2412db3897fcdac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301263648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9608da56aa721891e00a668529a310f12455c860f9a3642bb2797e346806d30`
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
# Tue, 21 Apr 2026 23:03:07 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:03:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 21 Apr 2026 23:03:07 GMT
CMD ["jshell"]
# Tue, 21 Apr 2026 23:53:52 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:53:53 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 23:53:53 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 23:53:53 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 23:53:53 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 23:53:53 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 23:53:53 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 23:53:54 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 23:53:54 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 23:53:54 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 23:53:54 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 23:53:54 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 23:53:54 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778bbde58a3ca229166e8cb0daa518b00e18094f931f78db9a7788514823012f`  
		Last Modified: Tue, 21 Apr 2026 23:03:54 GMT  
		Size: 227.6 MB (227640423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd92469e04e332117c20bf4d6b381c1782edbdd6e668d2792d5a53b7f9510ad3`  
		Last Modified: Tue, 21 Apr 2026 23:54:28 GMT  
		Size: 30.0 MB (29995790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a08dcc7457e6e069ed5dab311b4f8fe95290d5bf9f35c96570ff5c774cd71d`  
		Last Modified: Tue, 21 Apr 2026 23:54:27 GMT  
		Size: 9.3 MB (9312252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed803d7b9a8853191a3bba20d6a02c80ad87ddefc8b2fafb453bdcd70408c02`  
		Last Modified: Tue, 21 Apr 2026 23:54:27 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14374a90c4a305dbc4d0604116d1d686a9dc27f1386542b43912d9ec965c00f8`  
		Last Modified: Tue, 21 Apr 2026 23:54:26 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:4f91024d61daa89ec8fae6321aabb6539e1c8b426ecf5da3f7da0d264c258342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ce58e9cf494bdba23b2e11bd51c6f331c97f8086b4591c442b94d7f93d32544`

```dockerfile
```

-	Layers:
	-	`sha256:d3818a85a4a9928b432a6f3edcb53f10a912fe54e8a20901355737228086e3a7`  
		Last Modified: Tue, 21 Apr 2026 23:54:27 GMT  
		Size: 4.3 MB (4311024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0488b9576c20c2a5a9919c0d87a31b7c9873873ec39ee9f70f446e1e6cb1f49f`  
		Last Modified: Tue, 21 Apr 2026 23:54:26 GMT  
		Size: 16.0 KB (15981 bytes)  
		MIME: application/vnd.in-toto+json
