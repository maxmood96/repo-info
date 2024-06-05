## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:234d59d147388eeb0d29fd1f44309791ddfda135b1e3a4f1ff667480cf310567
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:e3018a8439417ac955448a156b128ff299f31ff2d19975b0a9625e4359a71f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145267869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b8dd6c94dd237f3eff59f4b66708d679318d96d778ff2bdc5147a69d0048e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 23 Apr 2024 15:38:09 GMT
ARG RELEASE
# Tue, 23 Apr 2024 15:38:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 15:38:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 15:38:09 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 23 Apr 2024 15:38:09 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Tue, 23 Apr 2024 15:38:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 15:38:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Apr 2024 15:38:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENV KAPACITOR_VERSION=1.7.4
# Tue, 23 Apr 2024 15:38:09 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 23 Apr 2024 15:38:09 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 23 Apr 2024 15:38:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Apr 2024 15:38:09 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150f13846cf34d9eba8c200d495ef1665928c9e544e261c5a620a9da75d92943`  
		Last Modified: Wed, 05 Jun 2024 04:48:07 GMT  
		Size: 7.1 MB (7122433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5be799cda588480c8300d57f69898f300466dae9eed73a1251b4c1d5a5005ea`  
		Last Modified: Wed, 05 Jun 2024 06:10:54 GMT  
		Size: 36.3 MB (36328715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db34f1ed1e53e0f2aa29d6edadfdb9b335d46bcf690d82039ee812272203cdfe`  
		Last Modified: Wed, 05 Jun 2024 06:10:55 GMT  
		Size: 71.4 MB (71376918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa72120dc2b93b6106ec5d17dcd5b6c133ba52245ef251acac1cd1bd133c4499`  
		Last Modified: Wed, 05 Jun 2024 06:10:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb3e6f643b101eae42db42901637907ed9631737a6ea9c932740a105fbb629a`  
		Last Modified: Wed, 05 Jun 2024 06:10:53 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:9294f45146b3dbfd2ac0f1f10b4370bc8d0502d704bd94835be0a7b232045783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e431049eebc769bcf1b8a800c8d0a11a7d56984fb98d474b9a55c38cffef2892`

```dockerfile
```

-	Layers:
	-	`sha256:d7da001761cde84cc702eb55bfa0270c5ef2c84e718aafc27722891cb2e997b5`  
		Last Modified: Wed, 05 Jun 2024 06:10:53 GMT  
		Size: 3.5 MB (3476146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d56609f319a72df820f7defe2bd8f9ea5805e3cb5f9be7ab7e6cfd836689ff9`  
		Last Modified: Wed, 05 Jun 2024 06:10:52 GMT  
		Size: 14.9 KB (14859 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:0808fc7bd0ffec547ee0c684b0e4e88f3cfe93bcfdc3446ca2d85e552a8a30b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135651913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e19907e0e709f99d6ad2bc2f03f8d1b80ac8c894adbfb4ea8a08224d4f804d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 23 Apr 2024 15:38:09 GMT
ARG RELEASE
# Tue, 23 Apr 2024 15:38:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 15:38:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 15:38:09 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 23 Apr 2024 15:38:09 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Tue, 23 Apr 2024 15:38:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 15:38:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Apr 2024 15:38:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENV KAPACITOR_VERSION=1.7.4
# Tue, 23 Apr 2024 15:38:09 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 23 Apr 2024 15:38:09 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 23 Apr 2024 15:38:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Apr 2024 15:38:09 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed2234813e59f6b9eaee624a5527eb3d094518832c14eb4afbece4c0120a0c7`  
		Last Modified: Thu, 02 May 2024 03:32:04 GMT  
		Size: 7.1 MB (7068550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8ab3af51f539e7423de5232a8423a9dfc583130ea8e3729fd917e29677cb4c`  
		Last Modified: Thu, 02 May 2024 11:28:58 GMT  
		Size: 33.1 MB (33086682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65dc8207f2592544cbacf9a713abdfb98d0d2072b7ae02cba082f042417eaf8b`  
		Last Modified: Thu, 02 May 2024 11:29:31 GMT  
		Size: 67.1 MB (67094970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711a5bf32b8de2e4bb05f4dc0449160e5b1a95926501e0b2cda3c89e1fad3fbb`  
		Last Modified: Thu, 02 May 2024 11:29:30 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c578433905e794395fab461306112019f1083518d0fb977af233065da7a38f46`  
		Last Modified: Wed, 01 May 2024 22:32:20 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:c160a03fe092484cc1721bf8a0270261268362128058b782e831a0ec32f39dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3490600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432f1b85b7eb6393ff6a125bdfa64da5698aaa47881368dcc7cc72c9ab026547`

```dockerfile
```

-	Layers:
	-	`sha256:59663fac02f31131d39cee42053c9c157db312c4dc0c16147d026972a04e6f35`  
		Last Modified: Thu, 02 May 2024 11:29:30 GMT  
		Size: 3.5 MB (3475734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9fbacd00dd72774f124887afb8a6654395919cab16557b4d359f7385454bb76`  
		Last Modified: Thu, 02 May 2024 11:29:29 GMT  
		Size: 14.9 KB (14866 bytes)  
		MIME: application/vnd.in-toto+json
