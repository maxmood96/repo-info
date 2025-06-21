## `docker:rc-dind-rootless`

```console
$ docker pull docker@sha256:21c4e4145f4f07da5ce63476147beab9c9d8be9b7b4f9dbadf57576048326579
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:rc-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:11e59013b452198b82d0de475090bd9336737ca9532b83f53511dfa594540303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163474585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f960a82e89100f20353ea9555bc93b8e51273d5ad5573a880741d70c57f428b`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 16 Jun 2025 17:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
ENV DOCKER_VERSION=28.3.0-rc.1
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.3.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.3.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.2
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-x86_64'; 			sha256='95db7bb2ed5d5fc790a12559b9092d641637c2d0190939c282b52a7af572a8a7'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-armv6'; 			sha256='863412d376cb1341e2a6889aa58dc4b674a58350ceccc357c71284109a5cb4a2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-armv7'; 			sha256='33aa26709150e835992a8af58d590e32151473f78daea549ccd70bd5f96c3bbf'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-aarch64'; 			sha256='d2c195cf553e55d06761c192133a6a7b4d67d275c7f5ce673bbf8ecf20814061'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-ppc64le'; 			sha256='6c72243b9585cc741c8e90937fd28ca2c8f2fee8a7636b30d1bbf312df27e157'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-riscv64'; 			sha256='8448828a5fa46170b92fec62d928b753ba91e86cccace24a04187324b65836ac'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-s390x'; 			sha256='39d47d8aa2cec059b4dc5e9b627a1176bcce33d9090f237806cf59264fe55e89'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 16 Jun 2025 17:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Jun 2025 17:04:22 GMT
CMD ["sh"]
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.3.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.3.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 16 Jun 2025 17:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 16 Jun 2025 17:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 16 Jun 2025 17:04:22 GMT
CMD []
# Mon, 16 Jun 2025 17:04:22 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-28.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-28.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 16 Jun 2025 17:04:22 GMT
USER rootless
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24b25e004d4867df8e9bf0324bf4d49a3ed9d26c566af3c69a6ece667cdd4d1`  
		Last Modified: Fri, 20 Jun 2025 19:46:35 GMT  
		Size: 8.2 MB (8207454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed7b3b3424b2f3627c5c7b88bd9dc656167d18358b1211de725e224aede6ced`  
		Last Modified: Fri, 20 Jun 2025 19:46:31 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf79ea00eefa87bf1fa4bdae44f4d91182fc627123d4a7a58d95a5e9256c4bd7`  
		Last Modified: Fri, 20 Jun 2025 19:46:32 GMT  
		Size: 20.4 MB (20449419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51146fa69b36c259dc9d3d4982b64d97e0aba79940cc20e463604ee2f76ee30f`  
		Last Modified: Fri, 20 Jun 2025 19:46:34 GMT  
		Size: 21.7 MB (21664160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a6e3bb58f0ed305c3089d1005149354b86e045a63d53eaca8bd21b242db46a`  
		Last Modified: Fri, 20 Jun 2025 19:46:35 GMT  
		Size: 21.3 MB (21253094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78ac15c753d03fb45dc128620313c5a6255b9fddbe608dea405ac40dc3a0db2`  
		Last Modified: Fri, 20 Jun 2025 19:46:25 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267183a39bafcd62e9ec9c6903f7b92837941af2459e45683c6c2e7611aff7e1`  
		Last Modified: Fri, 20 Jun 2025 19:46:26 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8117b6b5c9054f6422e5e9544a562400d561ed596bb77ec953701bdc4e37a985`  
		Last Modified: Fri, 20 Jun 2025 19:46:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f27bff2dee9feeb0df47f42c5fcc3ba04ab31b769be84709d65dce433990ee`  
		Last Modified: Fri, 20 Jun 2025 20:07:05 GMT  
		Size: 6.9 MB (6905602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083d0e279e035a06a72cd9541ff282ba57e5756e82989f40d78413ce2ca997b2`  
		Last Modified: Fri, 20 Jun 2025 20:07:04 GMT  
		Size: 90.5 KB (90488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4cf95678810482cb92fd0ce72b21dd43dedf91b4ec84bc6e281df8b3d82ddb`  
		Last Modified: Fri, 20 Jun 2025 20:07:05 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb61a674db4704b6aed9d5c342b3d3d29657ac198e4ad46ce5f5f5696e088b06`  
		Last Modified: Fri, 20 Jun 2025 20:07:10 GMT  
		Size: 62.5 MB (62518568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c13fb02bfa43da22251e2dc09863af0a6c2ff739726990a6b193ee095eb9c8`  
		Last Modified: Fri, 20 Jun 2025 20:07:06 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56cfddfd417995c4b455799efa7211a4084996ab96fd656d12ff3041aad3c5a8`  
		Last Modified: Fri, 20 Jun 2025 20:07:07 GMT  
		Size: 3.3 KB (3298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ae4a9fc7c29606f1d3e667bb0a643c320e16cf8e59d1565d2a12c7ee0e2a4c`  
		Last Modified: Fri, 20 Jun 2025 22:02:32 GMT  
		Size: 993.3 KB (993278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d7b86dbe62093bd9405c8678f46de6e4f62841f425dcc8a412211446493aea`  
		Last Modified: Fri, 20 Jun 2025 22:03:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f959a079732b1aa5f94eb4ccb67593a4e9f3381c2148db5d66548ee0b8a91a`  
		Last Modified: Fri, 20 Jun 2025 22:04:05 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9803e3dc76a5bb6fbd0c063f813472be100a44d5c22ee69db90ec73668485cb9`  
		Last Modified: Fri, 20 Jun 2025 23:08:35 GMT  
		Size: 17.6 MB (17586177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ae19e88495a3505c06402ecb188d238bacdb9ee18acdd2a3dfa9cb8f2b370b`  
		Last Modified: Fri, 20 Jun 2025 22:04:10 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:e516d3aca757111178d2c781330662b10b4863bc011aee62de348f4aeaa17fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 KB (30204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729753296b0954cc3370d315f9d0ab65363517d5aa7cd778d6a255c3938bf986`

```dockerfile
```

-	Layers:
	-	`sha256:148c2b6ce36e294eede1f1a22f6b96f9eff8007001e31137b6ec35ed0bab65f7`  
		Last Modified: Fri, 20 Jun 2025 23:08:22 GMT  
		Size: 30.2 KB (30204 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:rc-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:dd23c2ade97eabad45368395f551b5f8709fa7051542a72f0d7bc7dca4b058ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154675161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e588db309e0b25ebbed17672da2e139943bd0aa9309e220ef4753085b20c9b89`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 16 Jun 2025 17:04:22 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
ENV DOCKER_VERSION=28.3.0-rc.1
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.3.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.3.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
ENV DOCKER_BUILDX_VERSION=0.25.0
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-amd64'; 			sha256='4104d79a791a8744c0b43fd5bd0a6172dff29040c5229946a1cdb2d27b0b5bfa'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v6'; 			sha256='4b92125aa797875108174d9d8ae2e92bdf1db82c97dcf8b3bb72490a62fd8122'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm-v7'; 			sha256='0c943fa7001cde147ab7663e36c92259ddde2a3ce0b6f5dfcbc3535dc67f8661'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-arm64'; 			sha256='f07063844bb750172c1f25cef61b07a8314d24bedffc015517b3ec4016b16de8'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-ppc64le'; 			sha256='9ac89d1401b105be41e98760aaaae00e4f44e180e757bf6044d2824ff14788bf'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-riscv64'; 			sha256='17829ab06c8ec984201170bfb676e6cd311312983814354505fb679b36c02177'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.25.0/buildx-v0.25.0.linux-s390x'; 			sha256='1b4a7d86fee5b6a48fd153418bd6ed8f0c82bc5d7eb3b219052e834ece977440'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
ENV DOCKER_COMPOSE_VERSION=2.37.2
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-x86_64'; 			sha256='95db7bb2ed5d5fc790a12559b9092d641637c2d0190939c282b52a7af572a8a7'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-armv6'; 			sha256='863412d376cb1341e2a6889aa58dc4b674a58350ceccc357c71284109a5cb4a2'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-armv7'; 			sha256='33aa26709150e835992a8af58d590e32151473f78daea549ccd70bd5f96c3bbf'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-aarch64'; 			sha256='d2c195cf553e55d06761c192133a6a7b4d67d275c7f5ce673bbf8ecf20814061'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-ppc64le'; 			sha256='6c72243b9585cc741c8e90937fd28ca2c8f2fee8a7636b30d1bbf312df27e157'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-riscv64'; 			sha256='8448828a5fa46170b92fec62d928b753ba91e86cccace24a04187324b65836ac'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.37.2/docker-compose-linux-s390x'; 			sha256='39d47d8aa2cec059b4dc5e9b627a1176bcce33d9090f237806cf59264fe55e89'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 16 Jun 2025 17:04:22 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Jun 2025 17:04:22 GMT
CMD ["sh"]
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-28.3.0-rc.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/test/armel/docker-28.3.0-rc.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/test/armhf/docker-28.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-28.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
VOLUME [/var/lib/docker]
# Mon, 16 Jun 2025 17:04:22 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 16 Jun 2025 17:04:22 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 16 Jun 2025 17:04:22 GMT
CMD []
# Mon, 16 Jun 2025 17:04:22 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/test/x86_64/docker-rootless-extras-28.3.0-rc.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/test/aarch64/docker-rootless-extras-28.3.0-rc.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 16 Jun 2025 17:04:22 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 16 Jun 2025 17:04:22 GMT
USER rootless
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87dd1a3f6c33f5cb4f37f8a56f360f53067b0e0c52a924ced150a71eab35066c`  
		Last Modified: Fri, 20 Jun 2025 20:04:23 GMT  
		Size: 8.2 MB (8229008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7ed8201efef3688d822f65774ebbec704be1fc5c71723142c2628f11933482`  
		Last Modified: Fri, 20 Jun 2025 20:04:22 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e78bf25dca30752d82e6bddad59edc9899c6fdcb877d7a16d85f0f38cce0369`  
		Last Modified: Fri, 20 Jun 2025 20:04:25 GMT  
		Size: 19.3 MB (19258549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d7a71f18a9bfeb3b114e6e1a961e864dad04504c6a90f0437ff8f7695eec14`  
		Last Modified: Fri, 20 Jun 2025 20:04:25 GMT  
		Size: 19.8 MB (19819435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce0534fae0833a84160e165b0eda0a2f609736bb468f1f0df36eec2f01b4fe1`  
		Last Modified: Fri, 20 Jun 2025 20:04:24 GMT  
		Size: 19.5 MB (19486792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f76b94e03cee9aeaf6952edd25fb087b82db9f71d7e705d84e0a134a439bfa9`  
		Last Modified: Fri, 20 Jun 2025 20:04:23 GMT  
		Size: 538.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3d6e68218c305c7763fc5dde69d9f85cde732d7a25ecce44ae55f02e82d038`  
		Last Modified: Fri, 20 Jun 2025 20:04:23 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb123f0f3894ccb3286ad43cf84efe72bbbb7d16227006454d96ec7fd7ccdcf`  
		Last Modified: Fri, 20 Jun 2025 20:04:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c8bffee4b1871506db435ed08f5809bdcb2b6ccfbbd5efb6db89c55a42b225`  
		Last Modified: Fri, 20 Jun 2025 20:59:46 GMT  
		Size: 7.1 MB (7141572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175c36f89a8366c0e9d16333d0cb84d446325ac924a470f6cde2ae22c6961f0e`  
		Last Modified: Fri, 20 Jun 2025 20:59:46 GMT  
		Size: 99.6 KB (99631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac75aacb69d0878eee1d17fbea4154f2eb80adf3ab98134f9b1680b05987998`  
		Last Modified: Fri, 20 Jun 2025 20:59:47 GMT  
		Size: 1.0 KB (1011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de048cad6560308108f27699f6de2c72bacd55fd16054a8a40a3ba338dc2204`  
		Last Modified: Fri, 20 Jun 2025 21:07:15 GMT  
		Size: 57.5 MB (57454408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965abae6a97c0afe00d6d85b116cbd3fe95ca2545bf2cdbf08ea37441feb46d5`  
		Last Modified: Fri, 20 Jun 2025 20:59:47 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bfc2b784b38828770e821740c09a11cf33727e5c4a02bfbf5e10e8bf023034`  
		Last Modified: Fri, 20 Jun 2025 20:59:47 GMT  
		Size: 3.3 KB (3300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2307f3870fe2fb72787d4abdb880794e851d3e606afbe99e79184a08afa65f`  
		Last Modified: Fri, 20 Jun 2025 21:08:34 GMT  
		Size: 1.0 MB (1023003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0168dd8a10639a98de32d94fad534a40941921be57605b5b03611bfd613d674`  
		Last Modified: Fri, 20 Jun 2025 21:08:34 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b44635e4769ace6eab0bdcb5b64edeb5d1f1b18d63d9c85be0724e809c2cf4`  
		Last Modified: Fri, 20 Jun 2025 21:08:34 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09dec240edca82bffddd2db1435528c86fdd0116b8e3605fb3c4101d95b6364`  
		Last Modified: Fri, 20 Jun 2025 21:08:36 GMT  
		Size: 18.0 MB (18017324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef099bc0a9ae11552592ec9d9a42046d55fc2f01856e1c5c134448313d5cb4e`  
		Last Modified: Fri, 20 Jun 2025 21:08:34 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:rc-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:99ab320193ac592a0297fa3845e602258c333cdf3005159a7acf39956d26a8e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 KB (30361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b34dec8016da6aad3afee04c177b9e09cb250a4496802e3fb40dc50589f303`

```dockerfile
```

-	Layers:
	-	`sha256:39b5ade5b3bd0a58b01bcb0dd53cf11cf859fb7b706310fae284a8e7cf9cc639`  
		Last Modified: Fri, 20 Jun 2025 23:08:27 GMT  
		Size: 30.4 KB (30361 bytes)  
		MIME: application/vnd.in-toto+json
