## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:0b6484788454c27683886a3b1cbb7ff25abd7d3589ce8ecfda7b317815cfbc11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:611d0cf9b5f641bbb13796b522d4780391689f70887849ad28c900ef053409fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.2 MB (152176109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9a0017c1208e9c9a2ba664fdb98f01650d752c44e74ec2a5202942ef02ec46`
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
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 13:09:59 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENV KAPACITOR_VERSION=1.7.7
# Wed, 28 May 2025 13:09:59 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 28 May 2025 13:09:59 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 28 May 2025 13:09:59 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 28 May 2025 13:09:59 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 28 May 2025 13:09:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 13:09:59 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a371f1ee9522de0fd813c4772011abcbcdbb8f39e3cf1285f265032957183988`  
		Last Modified: Mon, 05 May 2025 16:34:22 GMT  
		Size: 7.1 MB (7102973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754cbdb4b2c2391a3205d60ca8e4ebd2a9ee1b1b8f16c20a7a7698a8bbcf4cbd`  
		Last Modified: Wed, 28 May 2025 23:10:03 GMT  
		Size: 43.5 MB (43488806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77137f75b04ccb5eae8075f9b5e1ee2dc7270fc23a54da57ab34dd6d77337e9`  
		Last Modified: Wed, 28 May 2025 23:10:03 GMT  
		Size: 72.1 MB (72051194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e0fbafe873ad1b0ff14603a311e84845c5f20c51d593bd5e8df84a5195f874`  
		Last Modified: Wed, 28 May 2025 23:10:02 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daada038371a3217edfa1321b2506337b4a829acd73dfe17c25decdf6b5b0958`  
		Last Modified: Wed, 28 May 2025 23:10:02 GMT  
		Size: 295.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:8fb860c0936879821e1427f2209faf6ba8ca24ab481d67c319bbb20f8d59421a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3597721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7422e86e90f63963314413b1985eed6ec4310568fb686a130b9e39fefc8d956`

```dockerfile
```

-	Layers:
	-	`sha256:0307ca7c900927e51ac78f39f9ea24c9ac6a07c8b95fc70f733fe4776e15d6b0`  
		Last Modified: Wed, 28 May 2025 23:10:02 GMT  
		Size: 3.6 MB (3582658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7edfaa87ca850ae8d0702eb04dc84a47d55176bccbb40a819bf67915195efbda`  
		Last Modified: Wed, 28 May 2025 23:10:02 GMT  
		Size: 15.1 KB (15063 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:9a4029ed77eee67bc081478d4b81650f81913c79eced50af1c5dc4ef0e6cfd24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142847392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43aae85ed6be3e220f0204e8bdc0ab14bf4f75458bbe4c4f2a84775030706bb`
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
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 13:09:59 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENV KAPACITOR_VERSION=1.7.7
# Wed, 28 May 2025 13:09:59 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 28 May 2025 13:09:59 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 28 May 2025 13:09:59 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 28 May 2025 13:09:59 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 28 May 2025 13:09:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 May 2025 13:09:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 May 2025 13:09:59 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8d379476072addecd776a689c342eba7552fd3b54d1d640a45b2d23c18df19`  
		Last Modified: Mon, 05 May 2025 16:36:00 GMT  
		Size: 7.0 MB (7049030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c05201f0c21400c233526b64a20db03271e48fc6ac776017f714f8b02be083a`  
		Last Modified: Wed, 28 May 2025 23:09:12 GMT  
		Size: 40.6 MB (40629854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afc713541b7e66c901cbc80c79dc5cf5d60cc3fbd26ea02e73f0388d99c40d3`  
		Last Modified: Wed, 28 May 2025 23:09:13 GMT  
		Size: 67.8 MB (67813776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df96e6c6adafe24561355eea7ef49c482975e15d0ff559462c53031920fb2178`  
		Last Modified: Wed, 28 May 2025 23:09:10 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841e0b648f08b2f1ac40a44f20f854e09ef55cff24d2c45a40e2008549bbba19`  
		Last Modified: Wed, 28 May 2025 23:09:10 GMT  
		Size: 295.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:895da0fdd0e91ff331c329de68935ea279eacc1ba24277f13fa12c6a126c905e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3597302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf80a361ffa1fb478a7a40ae6582ef8652f88e03267d9e8ae6ea959c6d4f3b8`

```dockerfile
```

-	Layers:
	-	`sha256:0e804530c1bdc958e017c2fd0e47463b6857da35821213be551afd9359125bdb`  
		Last Modified: Wed, 28 May 2025 23:09:11 GMT  
		Size: 3.6 MB (3582132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1008259893dc1d08205fda1500f0134de332205b142348391a0812fea6012d67`  
		Last Modified: Wed, 28 May 2025 23:09:10 GMT  
		Size: 15.2 KB (15170 bytes)  
		MIME: application/vnd.in-toto+json
