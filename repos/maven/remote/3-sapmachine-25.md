## `maven:3-sapmachine-25`

```console
$ docker pull maven@sha256:85c2cbf5d6f38dedf2967e3ac619b0c666816503aed8f948a3145c2a4547f051
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
$ docker pull maven@sha256:91bb9bb4a2f83dcd57d2145d8bb6af8296987dc70ac38bf3cfb2474c757cf22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.8 MB (286754272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b26925bd1836804d8b91724e15beb0675f7240f7727db026c728da68ff620c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:23:38 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:23:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 02 Jun 2026 08:23:38 GMT
CMD ["jshell"]
# Tue, 02 Jun 2026 10:30:18 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:30:18 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 02 Jun 2026 10:30:18 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:30:18 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:30:18 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 02 Jun 2026 10:30:18 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 02 Jun 2026 10:30:18 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 02 Jun 2026 10:30:18 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:30:18 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 02 Jun 2026 10:30:18 GMT
ARG USER_HOME_DIR=/root
# Tue, 02 Jun 2026 10:30:18 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 02 Jun 2026 10:30:18 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 02 Jun 2026 10:30:18 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa649e9ce4f60c8cdc1d760f349bbb0a9d0a85f488106f347e76ac8c7f72c7b2`  
		Last Modified: Tue, 02 Jun 2026 08:24:00 GMT  
		Size: 222.2 MB (222186544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930c5ea86b1e431844c783857ae72d5c1587e0c504f975b3adbb84c3afb0deec`  
		Last Modified: Tue, 02 Jun 2026 10:30:32 GMT  
		Size: 25.5 MB (25473949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8996abebe876e6547c800d626bee1a554145c3512b828c45604838aedb97f2d9`  
		Last Modified: Tue, 02 Jun 2026 10:30:32 GMT  
		Size: 9.4 MB (9359966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1d34720fc5f894f221cff115809c3a7657cd047585530bdfc7171bd85f42a2`  
		Last Modified: Tue, 02 Jun 2026 10:30:31 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a10bbeff2f0852493589afb801d9b58753f034dbc081092755485effd89480`  
		Last Modified: Tue, 02 Jun 2026 10:30:31 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-25` - unknown; unknown

```console
$ docker pull maven@sha256:dbed987364e64db92067aff262139b49843ccbd9db5a5e2b0349c0b82a809db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8fcc2bc5da18bcc148af360d1962009f5a8d400623215fdfa474b9e19f5300`

```dockerfile
```

-	Layers:
	-	`sha256:4fafd123bfd0566085dbeef999a6b6e911f3ce7fb7c3911b734dbadf8e09f028`  
		Last Modified: Tue, 02 Jun 2026 10:30:32 GMT  
		Size: 4.3 MB (4312501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4f3ed4c39e82b966b24055e0dbb91f97285fe6fd9ff808bcd5007b29923aed7`  
		Last Modified: Tue, 02 Jun 2026 10:30:31 GMT  
		Size: 14.7 KB (14665 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-25` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:7f4a7e61aa90fcac6e7eef27cfae04eb0f075a1a3ad3d47f1bd734b153b249f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.8 MB (283763994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3104bb9fb80db21e512b259c2e610d7fa5c5b3c437c3d003a4854500e7671e2c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:23:53 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 02 Jun 2026 08:23:53 GMT
CMD ["jshell"]
# Tue, 02 Jun 2026 10:27:10 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 10:27:10 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 02 Jun 2026 10:27:10 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:27:10 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:27:10 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 02 Jun 2026 10:27:10 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 02 Jun 2026 10:27:10 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 02 Jun 2026 10:27:10 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:27:11 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 02 Jun 2026 10:27:11 GMT
ARG USER_HOME_DIR=/root
# Tue, 02 Jun 2026 10:27:11 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 02 Jun 2026 10:27:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 02 Jun 2026 10:27:11 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd31e39de7e7bdd6bd81ea1c2ff529e5d04625464d1994be7dbcfa1b81dabff`  
		Last Modified: Tue, 02 Jun 2026 08:24:19 GMT  
		Size: 220.0 MB (219990842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9984b03ddad8ec1f12b75873d435b6057e8c9551b9b01f44ceacb3a77f340572`  
		Last Modified: Tue, 02 Jun 2026 10:27:25 GMT  
		Size: 25.5 MB (25535771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939eb3553e3e09625fe69d7fb3a017259b2e1af92942464701b7917bec9e4a59`  
		Last Modified: Tue, 02 Jun 2026 10:27:24 GMT  
		Size: 9.4 MB (9359968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca811bf072a89158b5e6730d14e942357a09d37b142fb493abc3b4a35911ec99`  
		Last Modified: Tue, 02 Jun 2026 10:27:24 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6914f1cf50c2ec23b76488fa8dec93cdf542b085ec231dce9a81d4a2859dd4c4`  
		Last Modified: Tue, 02 Jun 2026 10:27:23 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-25` - unknown; unknown

```console
$ docker pull maven@sha256:2856380e2f8d928bb51e3613530b44f59d39d51d0c97614697c49e23377906ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4333818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f44603d10cac9fd7f2a947e9cdecf3e28f126309dd2c8d996ab3195301822840`

```dockerfile
```

-	Layers:
	-	`sha256:97335a81cfffebd57f981f1d2e1882e6aa60bbfaf4adc5cbf101772b207d32ff`  
		Last Modified: Tue, 02 Jun 2026 10:27:24 GMT  
		Size: 4.3 MB (4319020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bbe83846ab3c570aa1e47e97b26a719d1836cc64d23dce0ea7fbf3bd49bbb25`  
		Last Modified: Tue, 02 Jun 2026 10:27:24 GMT  
		Size: 14.8 KB (14798 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-25` - linux; ppc64le

```console
$ docker pull maven@sha256:6631a80b3a768a69bfd69c485126b1f7a1ce7fe3bd321197d685205eae887fe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296583420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712cc846e741258c70efc97e2144070854508f7a4ac5aa9b7d741697970a2bf5`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:54:09 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:54:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 02 Jun 2026 08:54:09 GMT
CMD ["jshell"]
# Tue, 02 Jun 2026 12:08:52 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 12:08:52 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 02 Jun 2026 12:08:52 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 12:08:52 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 12:08:52 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 02 Jun 2026 12:08:52 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 02 Jun 2026 12:08:52 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 02 Jun 2026 12:08:52 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 12:08:53 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 02 Jun 2026 12:08:53 GMT
ARG USER_HOME_DIR=/root
# Tue, 02 Jun 2026 12:08:53 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 02 Jun 2026 12:08:53 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 02 Jun 2026 12:08:53 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babd05d9b2bcefe17b564e5a2b8b5e01db7b30029df4a7fbe2e1d13c4505bbca`  
		Last Modified: Tue, 02 Jun 2026 08:54:58 GMT  
		Size: 222.9 MB (222907176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21802211222127fcb463627379de57f9290f861b76b61770a43f70698f265e9a`  
		Last Modified: Tue, 02 Jun 2026 12:09:27 GMT  
		Size: 30.0 MB (30001164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb241587a3a7a755423ff501e20e807e4f45374c8f90b1be8f63ecd2a2552d9`  
		Last Modified: Tue, 02 Jun 2026 12:09:26 GMT  
		Size: 9.4 MB (9359974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544b151ba20a1acdb2ca282212bb5a0f9f1964efedb778c3f6928ddc6e97a105`  
		Last Modified: Tue, 02 Jun 2026 12:09:26 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d8ef46b298f2b118a9efd9363ba14c0dcff6f8f61ed7ae4802017fc07f33ba`  
		Last Modified: Tue, 02 Jun 2026 12:09:25 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-25` - unknown; unknown

```console
$ docker pull maven@sha256:335a74268dc876f5d097578d31b77b5dfc330d671e8f6d315bb17731cd8a2e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4327027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75951b905d4e2c419c84cdcbddcc2e409c7cb9067119dca4f230af588738545b`

```dockerfile
```

-	Layers:
	-	`sha256:1492da442f553fddc45eac240a668a1de84a9ecae1ddc016778363c31e051709`  
		Last Modified: Tue, 02 Jun 2026 12:09:26 GMT  
		Size: 4.3 MB (4312312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc89c16730b29f6ae92b65b9388527a8fc7c32c3e0a33e8bdc4b090e8a8ebd1a`  
		Last Modified: Tue, 02 Jun 2026 12:09:25 GMT  
		Size: 14.7 KB (14715 bytes)  
		MIME: application/vnd.in-toto+json
