## `docker:24-dind-rootless`

```console
$ docker pull docker@sha256:31bed9fb513eac600d0a490d9dd71fdc4f31e95a576d907c259e9cd781719f0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:24-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:a7000229b8181e1702fb20732f5c683289bfb3973b457b60fd9b27f4e521bc36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142557085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb4ab934a09f6333189afe3d67c80b182a1a21b741a9752e30803129092f2e31`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 26 Oct 2023 17:04:13 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Thu, 26 Oct 2023 17:04:13 GMT
CMD ["/bin/sh"]
# Thu, 26 Oct 2023 17:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
ENV DOCKER_VERSION=24.0.7
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.2
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-x86_64'; 			sha256='067a12983b9333d01947329190af756b6d12afe7b4b51b3e1e29328b4afe3b9f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-armv6'; 			sha256='582d734ef0c14335ee4691f3550d56b3e1c1c4d787ed6354830b3c222eee542e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-armv7'; 			sha256='e83fa84dc73cc8d5a0fe2d1ad3ad61202050f033e6df9f3f4f7b3c2b59181006'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-aarch64'; 			sha256='beafe762fedd06fe9885317c33f8b29b39c2354d6840a494a69b3c3a36919212'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-ppc64le'; 			sha256='6be73d6597efc822eff3f9dd6abb56b72ada76f8a5f798b1df2dce5105f39257'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-riscv64'; 			sha256='33a15fcef9d975aee4ed404779fae068264da6de8f2851ead85f9e1701302411'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-s390x'; 			sha256='0b62a8d7aad7ce81220a4d77aa4b17e443b888248c1da22bc808db1fcbf1e9ac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Oct 2023 17:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Oct 2023 17:04:13 GMT
CMD ["sh"]
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
VOLUME [/var/lib/docker]
# Thu, 26 Oct 2023 17:04:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 26 Oct 2023 17:04:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 26 Oct 2023 17:04:13 GMT
CMD []
# Thu, 26 Oct 2023 17:04:13 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 26 Oct 2023 17:04:13 GMT
USER rootless
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef263e1cd754d13e6d9ce8d5a1adea24b930c3331673c02ad758ca13f608805`  
		Last Modified: Mon, 22 Jan 2024 22:50:03 GMT  
		Size: 2.0 MB (2018461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73157b7f59e797e588b85cafd95d2fabb4e5742fcc6ef90332fb8d18a6666083`  
		Last Modified: Mon, 22 Jan 2024 22:50:03 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4628406856b38dbb1c7ed330b729fba478a39fc6a930436d4f99dfdecf332c8e`  
		Last Modified: Mon, 22 Jan 2024 22:50:04 GMT  
		Size: 16.4 MB (16400381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e638496eda7597f8e428cf7f4a999a403883cf6443ff6404caa0b4fa519370`  
		Last Modified: Mon, 22 Jan 2024 22:50:04 GMT  
		Size: 17.2 MB (17195309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6db6571b5711b6c0bc060701100346c2d6f01760f25a0e1a3a92afff9f6f4a9`  
		Last Modified: Mon, 22 Jan 2024 22:50:05 GMT  
		Size: 18.2 MB (18175517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ad86912675a0dc3442a89c27bf5ab5c2401c0ef12bc5757b49a71c80c178c7`  
		Last Modified: Mon, 22 Jan 2024 22:50:04 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8910acd92400f14d6ac132bc271f070cfe0a9092cca2f0c1522d7f94ac9d7f`  
		Last Modified: Mon, 22 Jan 2024 22:50:05 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cda2ce493f365ff4b9207f7bfe048f9643d7ee217e7f96aeece317aea20165a`  
		Last Modified: Mon, 22 Jan 2024 22:50:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c42af7dec87ef5f0b5b3f9289f84870055b7be206cb842277173ca538295af7`  
		Last Modified: Mon, 22 Jan 2024 23:49:59 GMT  
		Size: 9.3 MB (9258273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57cc785c2be64fc0886124f42b6ab9f4d161c9e0e47b3440b7e6a5469b20b164`  
		Last Modified: Mon, 22 Jan 2024 23:49:59 GMT  
		Size: 83.6 KB (83645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b464165c77525700b437f1a2e28ab2d02e7fec53507e2c82f188b05b8bc343`  
		Last Modified: Mon, 22 Jan 2024 23:49:59 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41309ef45cf3172aa65dbfe7ea28e4ef3959f566a71d35a5b2fa64d07bafd9f9`  
		Last Modified: Mon, 22 Jan 2024 23:50:02 GMT  
		Size: 54.4 MB (54371642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea349de5085ab87ee4c700f2723c98c3955179a66e46a09433544a50f8900daa`  
		Last Modified: Mon, 22 Jan 2024 23:50:00 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69510923d28c04476929b21a2b57c2e403152b532f5985f4e6bdfd26db07df2d`  
		Last Modified: Mon, 22 Jan 2024 23:50:00 GMT  
		Size: 3.3 KB (3251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5084cdc41aa6e51d05cf42f8cabe5da6ae87f89cff4481441c94bc20dea52878`  
		Last Modified: Tue, 23 Jan 2024 00:48:57 GMT  
		Size: 974.0 KB (974045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da4565a77c0db58272e453932a3b4394ecd007c3a14ce958a91259d70b9f6e2`  
		Last Modified: Tue, 23 Jan 2024 00:48:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac61b065f465ba1e39fa9eaeed055f7fae4cf70c103353f0dc1f0e6ab2020b8b`  
		Last Modified: Tue, 23 Jan 2024 00:48:57 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b80bbd9990c1a0c2d30fb230ebd975ffbf004a549717e32f6f98bf12a4d54253`  
		Last Modified: Tue, 23 Jan 2024 00:48:58 GMT  
		Size: 20.7 MB (20661377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a9f6f819e0fcd540bcce441560f6cb83820e8a60451bf60cc531f87bbaf729`  
		Last Modified: Tue, 23 Jan 2024 00:48:58 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:ae91f14558a3c9bf04e2d92369312efb94118994313a9f09c202cfd6145f9478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **775.7 KB (775698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e16e54cda2bedec2cb348d106a3c2165689b6c9203692caa5226101ec687e7d1`

```dockerfile
```

-	Layers:
	-	`sha256:684f7911bf8148b5feb91828d7b82c6ab066971652aaf9829fb5b80828c0e446`  
		Last Modified: Tue, 23 Jan 2024 00:48:57 GMT  
		Size: 742.8 KB (742761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b3723a25728b1df98082409774cf0c8e37d281b65b251546369fb71760b8380`  
		Last Modified: Tue, 23 Jan 2024 00:48:56 GMT  
		Size: 32.9 KB (32937 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:24-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:85ac8ac59c64d3c8849400f3ed911baf845daebeb47fc07f3afea20639bd401a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135856361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62cc82021dc810f5c4f9683be581672f569a5bde5040c24786ce21254fd7f7bf`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 26 Oct 2023 17:04:13 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Thu, 26 Oct 2023 17:04:13 GMT
CMD ["/bin/sh"]
# Thu, 26 Oct 2023 17:04:13 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
ENV DOCKER_VERSION=24.0.7
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.1
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-x86_64'; 			sha256='d350bbbd1c74c0a8542193bd41881afea534b141c6a9d9a27b2f217e51d5c48c'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-armv6'; 			sha256='4a89b48f6a758793d4b40b1ade7bd9e7e2e177e29f05f74abb3fde08f246f0c8'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-armv7'; 			sha256='2b339b900447394b0cc985d9be30782361828b615ce743c36a9674d4435a2fb9'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-aarch64'; 			sha256='9b35494742cc54544cd3f67b162ebfb43435077f02556bfb5a7e1c543f0a2da7'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-ppc64le'; 			sha256='68ce36587759f18a9daaf4a11af6db1ba9e4b7089a8062654de38f8b84506647'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-riscv64'; 			sha256='b28cbb99ba1ae9d7b1a4e5d6828a2c2a9b124db2d4f1d226aa71a1f2741aa056'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.1/docker-compose-linux-s390x'; 			sha256='6177f40328d4004d37b7e422d102d765aeb03e24e202ca8b791a6c000be90665'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 26 Oct 2023 17:04:13 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Oct 2023 17:04:13 GMT
CMD ["sh"]
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
VOLUME [/var/lib/docker]
# Thu, 26 Oct 2023 17:04:13 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Thu, 26 Oct 2023 17:04:13 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 26 Oct 2023 17:04:13 GMT
CMD []
# Thu, 26 Oct 2023 17:04:13 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Thu, 26 Oct 2023 17:04:13 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 26 Oct 2023 17:04:13 GMT
USER rootless
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4959de38143abac793d31e4e8592696721305ff06281f8b9284aee380afcfe`  
		Last Modified: Thu, 14 Dec 2023 22:04:39 GMT  
		Size: 2.0 MB (2014899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf613c8d3eefad31faacee38beeedf68069e48ea01d8f083fa0a57ce343ed827`  
		Last Modified: Fri, 05 Jan 2024 02:15:00 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904cd2aef7e75dfb117f3229ae16a845ec7fc5a531dc4703c9570b506ea21c29`  
		Last Modified: Fri, 05 Jan 2024 02:15:27 GMT  
		Size: 15.4 MB (15449542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aae6e30004211f7085b9cfa27549866efabba965492a8541247e5bc3339d5aa`  
		Last Modified: Sat, 13 Jan 2024 02:34:42 GMT  
		Size: 15.6 MB (15640596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de362f7adeac693a52f24e7ecbd0bdf6bd901808412aede497f84423c946a1a`  
		Last Modified: Fri, 19 Jan 2024 02:42:23 GMT  
		Size: 16.6 MB (16610374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ff73bcf1fff1af5762af11a4d8746bb8e3a21bc9d167f87a39b4112e31df6c`  
		Last Modified: Fri, 19 Jan 2024 02:42:23 GMT  
		Size: 548.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403d7ccf9b3f3290dde8dbe88318f45b05afd72d645c6b3670eb587d732f7f40`  
		Last Modified: Fri, 19 Jan 2024 02:42:23 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d39d23bd07901fcdf3002ad5ec2f8f94b0898157e08a557470441f1ba843e2`  
		Last Modified: Fri, 19 Jan 2024 02:42:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e65db7609a682ae8ce3b5cbc00bac23cb6ceddabcc6ba4ffe3a4c55aa3483de`  
		Last Modified: Fri, 19 Jan 2024 03:37:53 GMT  
		Size: 9.5 MB (9509863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20066afa64e7739b041189c72758ef74f79c3131bf1197b04959686fc6b87050`  
		Last Modified: Fri, 19 Jan 2024 03:37:53 GMT  
		Size: 93.1 KB (93080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f85360c6682b53e35481c3ec3c5cdf71043fc8c0644346d4c929ba7abac5b2`  
		Last Modified: Fri, 19 Jan 2024 03:37:53 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70949971ca5fadae7249facf40d2af785620c832226ff5063fc44f7d32cf7b2`  
		Last Modified: Fri, 19 Jan 2024 03:37:54 GMT  
		Size: 49.7 MB (49711229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2c4dab19aaee07313b23b93ba1f11705c92db304209ee76658c336a78ca2dd`  
		Last Modified: Fri, 19 Jan 2024 03:37:54 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158bc3920765e3c179633b12d283ebdc51fe3cc5346da2dbafffeda6b57e958b`  
		Last Modified: Fri, 19 Jan 2024 03:37:54 GMT  
		Size: 3.2 KB (3250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e023d64792e05769289775079fe94e22f2b459509bd72ecca2000b6740c8062a`  
		Last Modified: Fri, 19 Jan 2024 04:40:14 GMT  
		Size: 1.0 MB (1016226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d23ff057320989234f250df1c963ccd14e95e68a7e99623a6c08b24d63aaac`  
		Last Modified: Fri, 19 Jan 2024 04:40:14 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b4a4aeaef90f173393670279987fe5d926c81244a101af55d9d50746662c49`  
		Last Modified: Fri, 19 Jan 2024 04:40:14 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd68458f4c34ab248562a3b133656363eb8be527cfa8f99ee4248f06a1bcf567`  
		Last Modified: Fri, 19 Jan 2024 04:40:15 GMT  
		Size: 22.5 MB (22452794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7678ce2c8715ede879fafe3372031089290a77e1cf81df2ee4cf192380d98f9`  
		Last Modified: Fri, 19 Jan 2024 04:40:15 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:24-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:3bbe5b00621444f0e228e276b0949e44ada57ec1d203a8119fa1aa34a36da7ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.0 KB (776036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c8845f18c785ccda92dc485469166096315c058884c9017ac7a81110d870bc`

```dockerfile
```

-	Layers:
	-	`sha256:c4bed9e3d120f2a13e0a50e6cbfb0202362d1eeb479f11ff9139aaf6ac5ded54`  
		Last Modified: Fri, 19 Jan 2024 04:40:13 GMT  
		Size: 742.7 KB (742724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe11a6cc7243112d81b524da1a04490662037a0211782acf11797677b34c0f1b`  
		Last Modified: Fri, 19 Jan 2024 04:40:13 GMT  
		Size: 33.3 KB (33312 bytes)  
		MIME: application/vnd.in-toto+json
