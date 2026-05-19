## `maven:3-sapmachine`

```console
$ docker pull maven@sha256:56c5c47c92ee46fa74901eca2266106561eb6f439fe60ba91d0d3c1aa3208fb3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-sapmachine` - linux; amd64

```console
$ docker pull maven@sha256:4dcbc4b004db1d9319aa9734ea670b1e430d5e54cb6ca64adbd07454c4277e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290945095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfede74b8698d665bdda24aeb935f38eae77c1d6d95a5929e806764eb2b941f5`
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
# Mon, 18 May 2026 22:42:43 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 May 2026 22:42:43 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 18 May 2026 22:42:43 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 18 May 2026 22:42:43 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 18 May 2026 22:42:43 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 18 May 2026 22:42:43 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 May 2026 22:42:43 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 May 2026 22:42:43 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 May 2026 22:42:43 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 May 2026 22:42:43 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 May 2026 22:42:43 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 May 2026 22:42:43 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 May 2026 22:42:43 GMT
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
	-	`sha256:c2589a400b2231be26c27a977ea3efd5a298db238a2bfdf8141e787d9377bbd1`  
		Last Modified: Mon, 18 May 2026 22:42:57 GMT  
		Size: 25.5 MB (25473847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af592aeb07cb19c6cf76f24b39b334ce29f5164a48ca715c9863aae5f8109b8d`  
		Last Modified: Mon, 18 May 2026 22:42:57 GMT  
		Size: 9.4 MB (9359980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0242c9432d186ebfb933c651249268a04af5918db8144ee4a8ada14b53227844`  
		Last Modified: Mon, 18 May 2026 22:42:56 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba41d1a030df22c1f80542d0c23b609c91d18502ace898ee4691531838dd34a`  
		Last Modified: Mon, 18 May 2026 22:42:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:f039a73cddc9ccbe51d418e0efce36accd1741eaa4655f6134686b94b61c38f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36dcb27bbd4bcbf1e8fdf4fcf60c1b9b7d5612834727da501a0cac554e766a53`

```dockerfile
```

-	Layers:
	-	`sha256:ef4207cce96e196865f87ec4d19b77588db6ebfa31fa3a535c85e29584512636`  
		Last Modified: Mon, 18 May 2026 22:42:56 GMT  
		Size: 4.3 MB (4311192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:144cf656489b6dc3fe8c4ddbab509b488a841ca9cfacc3577976819b9154650f`  
		Last Modified: Mon, 18 May 2026 22:42:56 GMT  
		Size: 15.9 KB (15906 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:8609822cc33b55ad8249c50a9fa19020a4a4decd95ddccb5cbbb1b6c2671a262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.0 MB (288018846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db8bde85024fc55f1d5c07e0425cdd7c8658d1e3b95485c8bd5847d30f0c521`
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
# Mon, 18 May 2026 22:42:47 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 May 2026 22:42:47 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 18 May 2026 22:42:47 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 18 May 2026 22:42:47 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 18 May 2026 22:42:47 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 18 May 2026 22:42:47 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 May 2026 22:42:47 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 May 2026 22:42:47 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 May 2026 22:42:47 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 May 2026 22:42:47 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 May 2026 22:42:47 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 May 2026 22:42:47 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 May 2026 22:42:47 GMT
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
	-	`sha256:810505949edcfe1e6506a946b5f8830f006a704829767858184ba5e647350250`  
		Last Modified: Mon, 18 May 2026 22:43:01 GMT  
		Size: 25.5 MB (25535745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd216c7b3ea7f5144b12a141e50ffe2d6ba0700ec83ce6574ce05671ddafc3a`  
		Last Modified: Mon, 18 May 2026 22:43:00 GMT  
		Size: 9.4 MB (9359977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87bcecadddf3536aa1b61723dc9804a9bd8bb8292a274f13f711fffaeb23e5cd`  
		Last Modified: Mon, 18 May 2026 22:43:00 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e90d2a72fdf7a58a76cce2ed316cd235f43ce47de72c242c75291b00b10a2e`  
		Last Modified: Mon, 18 May 2026 22:43:00 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:5ddcdebbe249162e81c8aab4373d6c4fd735dc50b1529cb4fcdbfacebc900552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4333847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab47d8209319a728a69a79479adde86112b26d4c131f1672cbbce21f7963294`

```dockerfile
```

-	Layers:
	-	`sha256:c8a8814c4e16c6f3e6bcb36f806beda5b4549861fa7c1bc30d23b063b013fedd`  
		Last Modified: Mon, 18 May 2026 22:43:00 GMT  
		Size: 4.3 MB (4317759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95dbaed9ae47d73d6ff2342c87d50ed81e2c06816970e4475659392bc4f9c1ad`  
		Last Modified: Mon, 18 May 2026 22:43:00 GMT  
		Size: 16.1 KB (16088 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine` - linux; ppc64le

```console
$ docker pull maven@sha256:28ee9d17442072630ecd34edaa39670bab269b6a549c2c68696644facc24a85b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301316783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3cdbeb7c74777dc7eb7200732b8dc26fd9cc692283dbbd77136639eadab579`
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
# Mon, 18 May 2026 22:43:51 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 May 2026 22:43:52 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 18 May 2026 22:43:52 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 18 May 2026 22:43:52 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 18 May 2026 22:43:52 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 18 May 2026 22:43:52 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 May 2026 22:43:52 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 May 2026 22:43:53 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 May 2026 22:43:53 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 May 2026 22:43:53 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 May 2026 22:43:53 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 May 2026 22:43:53 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 May 2026 22:43:53 GMT
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
	-	`sha256:b42bdfdb839881fd1f36952cf0995517d36cbb827fea5e6151efc5c17179944f`  
		Last Modified: Mon, 18 May 2026 22:44:21 GMT  
		Size: 30.0 MB (30001198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb139a5f5497588863dcfced61e37bcfab1158e0c811754e906c9fe1ebe42ee`  
		Last Modified: Mon, 18 May 2026 22:44:20 GMT  
		Size: 9.4 MB (9359977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d74e56e14e13fff7b568199224174601d4d5c2bd4c59fc3575a701351ebadc`  
		Last Modified: Mon, 18 May 2026 22:44:20 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a52ad0dbf2a880e53fd9017cabfba540fd187c094e576749e110925607bb35`  
		Last Modified: Mon, 18 May 2026 22:44:20 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine` - unknown; unknown

```console
$ docker pull maven@sha256:110240fe1cec6dd47fb22f0182d21038a6408a7fb998bb2419171a3b65d690a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa20c976271f5fefb713391545966921bff102fef068bb79a481c969a2bd7ed`

```dockerfile
```

-	Layers:
	-	`sha256:2ce775410e57cd9431997b52c22b44576b3535b55a13a8594550dba3492733f6`  
		Last Modified: Mon, 18 May 2026 22:44:20 GMT  
		Size: 4.3 MB (4311027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e2fe1a5e4fb08d3ff338e3fb9d9ffca08921dbe59608ff989aa28c3280a6c1`  
		Last Modified: Mon, 18 May 2026 22:44:20 GMT  
		Size: 16.0 KB (15981 bytes)  
		MIME: application/vnd.in-toto+json
