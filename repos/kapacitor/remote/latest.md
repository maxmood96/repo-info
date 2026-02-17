## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:7c0963201096a09318be3056c148a81359b1bc67cabbc72370a6c5573fda4c98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:64662f96d1a79000d87cc40e3351ddff98e9006c993678bc64433d652aac32c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174717519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab83ad65a72e9ddbfba143f549a91ba791f114b5b1dc602c335ab0939af7381`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:23:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 17 Feb 2026 21:23:46 GMT
ENV KAPACITOR_VERSION=1.8.2
# Tue, 17 Feb 2026 21:23:46 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 17 Feb 2026 21:23:46 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 17 Feb 2026 21:23:46 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 17 Feb 2026 21:23:46 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 17 Feb 2026 21:23:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 21:23:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 21:23:46 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541b91de6cf313637ee71aa147f2531502925472ffdf0e07e45b3dc2475d2a7b`  
		Last Modified: Tue, 17 Feb 2026 20:12:07 GMT  
		Size: 7.1 MB (7104256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab60e6561c6a7f9c21438b698ad15dcc4183be7610aa489d6068ef125debe89`  
		Last Modified: Tue, 17 Feb 2026 21:24:04 GMT  
		Size: 49.9 MB (49862612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1980b36be6d34e3df4657d184682066772b2fd592aa9bc41e93fbb4de35b5bb2`  
		Last Modified: Tue, 17 Feb 2026 21:24:06 GMT  
		Size: 88.2 MB (88212763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d17b7914e1280b7f8e2bee05ae18e7a76e83e8d4c0cf3127d27a613631b078`  
		Last Modified: Tue, 17 Feb 2026 21:24:02 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986ef5c1b9cfe6f61aa62954e1b0a398a3012f7867c3f3868fb96db505648bf0`  
		Last Modified: Tue, 17 Feb 2026 21:24:02 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:e13d7fa2dd962dd80a3e1ec736efce7253711caeb7dc7399a9fff2c797a68d5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38596f1029eabd691eb81a89f2cac6340d4c6706cfdcba15ff860f5fc8e51e1`

```dockerfile
```

-	Layers:
	-	`sha256:d2f801e066cc30314e5c64f6b0939bb24f630f1cb76c9d114e97c9081f6c8e36`  
		Last Modified: Tue, 17 Feb 2026 21:24:02 GMT  
		Size: 3.7 MB (3731269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6f33345dc3b22c1f915be1c8b627246419f73d6d92225841b1935c595a8371d`  
		Last Modified: Tue, 17 Feb 2026 21:24:01 GMT  
		Size: 15.0 KB (15019 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:7e8cb209d61301c0484554791cc9fdce260b21a2fce6f49c11142ba73137f4c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.8 MB (164846960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e7a9af661a48a139254be235889424adb9f4aca129cfc2285daaa452bde00f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:23:43 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 17 Feb 2026 21:23:49 GMT
ENV KAPACITOR_VERSION=1.8.2
# Tue, 17 Feb 2026 21:23:49 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 17 Feb 2026 21:23:49 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 17 Feb 2026 21:23:49 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 17 Feb 2026 21:23:49 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 17 Feb 2026 21:23:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 21:23:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 21:23:49 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4247dfca464006e30349fde79dc4e5d28c4c26f6afa234c81e4ce3fb42364f5a`  
		Last Modified: Tue, 17 Feb 2026 20:11:24 GMT  
		Size: 7.1 MB (7057616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe27530cabf66f1a2b0083fac3a2f24fab337b0cf0fbba537e9c79799306e97`  
		Last Modified: Tue, 17 Feb 2026 21:24:04 GMT  
		Size: 48.4 MB (48394168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb6ea0421fd0b281a72989a500c172318a53e71478a5cbd904758e8a9d05ffa`  
		Last Modified: Tue, 17 Feb 2026 21:24:05 GMT  
		Size: 82.0 MB (82009710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6a9e88f78d378ea4393de64e7e4ca1b4990913d65947090a140e8907f61b3d`  
		Last Modified: Tue, 17 Feb 2026 21:24:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa89b8b24717cac323da8cbef0d7808f06c623027f30ab428fc899d50312fc05`  
		Last Modified: Tue, 17 Feb 2026 21:24:03 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:0b26bc42605e300608b8f40266aa7d2bc8f2eeea188a918a19d802eef114698a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:086af4aa3167421d2847526f9085f708f7bec77e4071a6aadd71c69e4264b088`

```dockerfile
```

-	Layers:
	-	`sha256:fb24e1bcfd3a664680c22ee1589456a84b760f5a919d8de365dfc53cf6d4dfce`  
		Last Modified: Tue, 17 Feb 2026 21:24:03 GMT  
		Size: 3.7 MB (3730743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45f84043aeafd2098ee082b05fbd2362e3fd9d57e782239b391a71dd531dd1d0`  
		Last Modified: Tue, 17 Feb 2026 21:24:02 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json
