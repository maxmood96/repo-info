## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:a618b7837a8fa656d4039e977495f908d66c48f90f319461a9e1a572162f61e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:d9cc8f6f0c0322ebf70bcaefd6c42f39b935aaa4cd02c8c8ba6799369b4de0bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172695148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17757a7bf8d501e42b3890fef8dc82f852911deb91db187cb92b62fbe41c23b5`
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
# Wed, 11 Mar 2026 18:15:12 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 11 Mar 2026 18:15:19 GMT
ENV KAPACITOR_VERSION=1.8.3
# Wed, 11 Mar 2026 18:15:19 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 11 Mar 2026 18:15:19 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 11 Mar 2026 18:15:19 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 11 Mar 2026 18:15:19 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 11 Mar 2026 18:15:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 11 Mar 2026 18:15:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Mar 2026 18:15:19 GMT
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
	-	`sha256:45b85bd15b3ec606cc6214eb1cf42df087af9b0d7e35d394044415a11eb242c6`  
		Last Modified: Wed, 11 Mar 2026 18:15:39 GMT  
		Size: 50.3 MB (50335757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96698c2130ed223cd2480b0b063a7d64572a57ad09b9216fb587efd41e32b9d4`  
		Last Modified: Wed, 11 Mar 2026 18:15:40 GMT  
		Size: 85.7 MB (85717248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a7a5644b2dbe2a382c64ac2aa592f9a6159953b86f2945fe2cbac9b11ea9bc`  
		Last Modified: Wed, 11 Mar 2026 18:15:37 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770213e9d3d8b58603527bea7a2525e932450a53fed61e0d72266fb22940842a`  
		Last Modified: Wed, 11 Mar 2026 18:15:37 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:b3df88d06a4bf423029912709b30910996ca5266922c7e828b157c1119eeede1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3747046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59bd96b53ed67166744d3d5b88fb42950bfe1de8a6282b8d169db21d7680a5ee`

```dockerfile
```

-	Layers:
	-	`sha256:14f17cc39c23bf9f9ee83708ebbfe7171af603f4e76e93d716cfe85a7909d717`  
		Last Modified: Wed, 11 Mar 2026 18:15:37 GMT  
		Size: 3.7 MB (3732026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb0314381202be18c39f2547a8188612673ea78894384395a09c04c6ed682f14`  
		Last Modified: Wed, 11 Mar 2026 18:15:37 GMT  
		Size: 15.0 KB (15020 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:ba2d15e0e0701606ca04a4f328c28fb2a3636498a991e4c9860c9649de5aad3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163531596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f62a26a6b16ec8e0a4a845e110b594ad1bcf8a9524d7ac74589f01e2901447`
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
# Wed, 11 Mar 2026 18:15:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 11 Mar 2026 18:15:56 GMT
ENV KAPACITOR_VERSION=1.8.3
# Wed, 11 Mar 2026 18:15:56 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 11 Mar 2026 18:15:56 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 11 Mar 2026 18:15:56 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 11 Mar 2026 18:15:56 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 11 Mar 2026 18:15:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 11 Mar 2026 18:15:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Mar 2026 18:15:56 GMT
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
	-	`sha256:35ba0c2b4b790d5b53d3775fe8eb58e3942042c4918d57b53c634e6a451d529b`  
		Last Modified: Wed, 11 Mar 2026 18:16:16 GMT  
		Size: 48.9 MB (48944564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c2be56e0e0737c56ebdb64b0ca93699440d79f9f6e01530bf92c8e8f2cb1f7`  
		Last Modified: Wed, 11 Mar 2026 18:16:17 GMT  
		Size: 80.1 MB (80143951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52d8811656ec7a4e82b95582d34a0af9b0c591f2114574676ec8f9bb3c4424c`  
		Last Modified: Wed, 11 Mar 2026 18:16:14 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2c7bc879345937fe54133473126433893c79ab9a4b3a9f4dbc7394313bd4c2`  
		Last Modified: Wed, 11 Mar 2026 18:16:14 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:8d86fe778ce93f712a97e64f5bc8da6ce18ebf13bf03a9435d74e7dba6ee0780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9489bf7b5c63a970d711207f6df7cc23517fd18f6b2a16d1b8cb2c6b7ba902ae`

```dockerfile
```

-	Layers:
	-	`sha256:09978dca27a3d6d66eff490a4facfe882b3cc48cb729dda9e821f51ad4ef9ab8`  
		Last Modified: Wed, 11 Mar 2026 18:16:15 GMT  
		Size: 3.7 MB (3731500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c574a0f017064683fc9ab6f2f1df290b8b917562b335968f6bb4ce3d3a0166b6`  
		Last Modified: Wed, 11 Mar 2026 18:16:14 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json
