## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:8af2e0665c886fb74eab9699d0c5e181780b97ebc394602dad769d571b1178d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:23031a4049af462089444100e0ea41824b461a759c41ad682cc34ccba3a6ba1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172240899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e118bfd7c2c125b56a6af5962a32f8954f62dede9e3fe9598ffa9cac10566e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENV KAPACITOR_VERSION=1.8.2
# Mon, 29 Sep 2025 12:39:49 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 29 Sep 2025 12:39:49 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 29 Sep 2025 12:39:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 12:39:49 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a882c2cc2b3487f954b121776f38449e97c30ef32043eb9907c13c525178e473`  
		Last Modified: Thu, 02 Oct 2025 04:52:17 GMT  
		Size: 7.1 MB (7106046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2baee51d10ab242bbabf733dec920d0015113b400d7ae8c67d5035a28b277f5`  
		Last Modified: Thu, 02 Oct 2025 08:36:30 GMT  
		Size: 47.4 MB (47384790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb921dab1f7bdb605cb42ce6500764c079f9df48305ebdc58ddb038ff636a1e`  
		Last Modified: Thu, 02 Oct 2025 08:36:21 GMT  
		Size: 88.2 MB (88212722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678f567a9ff438c98e298b0aef4081302afa33ac81dbbad6f22eb6917d67b4b5`  
		Last Modified: Thu, 02 Oct 2025 08:36:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6a2bee9150f2d4212c5bed686fb4934ff97f1bb08718e6b156c8996a8b49aa`  
		Last Modified: Thu, 02 Oct 2025 08:36:16 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:9c9c5ed172664c8182f210b13fb7df231ff84948bd182ee3728d60afab8cbe63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc886c044e488c6e69ed8d7c70568b3a2954c385d81344e98487c3763b4d133`

```dockerfile
```

-	Layers:
	-	`sha256:9858f883ecd968d94ec2e1a7a47703f013277998ca3b3b78d546cbe48f135a32`  
		Last Modified: Thu, 02 Oct 2025 10:21:32 GMT  
		Size: 3.7 MB (3731269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c7ebac661d8ddc3ed5044c6b45c051a6d858bcbe8d19b4f94aad47568bae5e0`  
		Last Modified: Thu, 02 Oct 2025 10:21:33 GMT  
		Size: 15.1 KB (15063 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:c7a8eeb82ef4f15524e3cb6ae98cdfa36b641458c26265fe996d2c7f270146b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161696478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ee2f70ec439fcb8ecc2bf60125fcf970f471c8ce1ae545d72aa617b4787f45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENV KAPACITOR_VERSION=1.8.2
# Mon, 29 Sep 2025 12:39:49 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 29 Sep 2025 12:39:49 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 29 Sep 2025 12:39:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 12:39:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 12:39:49 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544fbec883712e8b92ee5a8fb96accd816f1bd25c1cb91370bc6a156f3923503`  
		Last Modified: Thu, 02 Oct 2025 01:11:19 GMT  
		Size: 7.1 MB (7052114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c027524204ede247971df3e55507c2a550b813d416efdf95e683767d420e91`  
		Last Modified: Thu, 02 Oct 2025 03:31:13 GMT  
		Size: 45.3 MB (45251049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca37f0340e18c9b768ee7d048b54cc869eb443c8fded3816cd4296ed0506e18`  
		Last Modified: Thu, 02 Oct 2025 03:31:18 GMT  
		Size: 82.0 MB (82009684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2ebbd0ee3cbb9593982f755e6c46b7c8d47e36f563d13b3af6f9f0055da32c`  
		Last Modified: Thu, 02 Oct 2025 03:11:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078fc759988b13ed983c52766c2e67f8a4b8f6b22d7c3b5d27eeca06ca2fe489`  
		Last Modified: Thu, 02 Oct 2025 03:11:26 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:3ba8b490ff1aa8ff3ddd28c5b889d312cd8fa4f6dedfe70a96b184f1a1c3d505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42e0499ba96e61ba17ddff758b7a0a21838df714f2fb9ddbf389dbd520d6256`

```dockerfile
```

-	Layers:
	-	`sha256:bc219b226c4662e9c83639d60188fe11bd7452b223036cd88061258d7904251c`  
		Last Modified: Thu, 02 Oct 2025 04:21:34 GMT  
		Size: 3.7 MB (3730743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d51b3667b4235134c87bb7cda0ae91c3a7f085ed9aced27459a7b9d071f34f4e`  
		Last Modified: Thu, 02 Oct 2025 04:21:35 GMT  
		Size: 15.2 KB (15170 bytes)  
		MIME: application/vnd.in-toto+json
