## `docker:26-dind-rootless`

```console
$ docker pull docker@sha256:56c377ddd669598492da153e8244f414cbde4314565d6bbb44ede6693b90caf6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:26-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:3ead427ca504b3cde1c9f8735017496baa5ea41fb52b5d7370ec09c6f25e5973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.9 MB (151917673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf9075dfad72415b5cc3d3a0228348da587c9baeca17ce09d93ed26e12df8d7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 05 Jun 2024 18:50:46 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Wed, 05 Jun 2024 18:50:46 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_VERSION=26.1.4
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.2
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-x86_64'; 			sha256='6fbaf6e93ccc43078a71a12db1d38224725cb5a9675391c38510355073f24066'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-armv6'; 			sha256='10b465c1771c262d372e24b09ed30fdc63687e35ae61c2365089e3998372a776'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-armv7'; 			sha256='b5bd40dfadf089617fe9cacb7a08d6fd5fae28e2a465191be1f25f22ffead344'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-aarch64'; 			sha256='de8c48203f4876fe3ae8bf27081a9aa69dc87de67a705f9d76c3a3ad776ed0c2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-ppc64le'; 			sha256='5810b3e6184032edbd21f12ed165ddecc823b8222ff5e4f6c55112af6f617c6d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-riscv64'; 			sha256='2c138daa9eaa909434c808018c4ab748a5f25caee16e3a7810fbeb3897b40878'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-s390x'; 			sha256='4084bdab8782e98c57a5f7aa7384699490048ce117dc7e70cad183702cc1645b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jun 2024 18:50:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
CMD ["sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
VOLUME [/var/lib/docker]
# Wed, 05 Jun 2024 18:50:46 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 05 Jun 2024 18:50:46 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
CMD []
# Wed, 05 Jun 2024 18:50:46 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-26.1.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-26.1.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 05 Jun 2024 18:50:46 GMT
USER rootless
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827ba70d82282d38791cfbb6472f5dee1cc82535772d92c60d37ae0a8572a348`  
		Last Modified: Thu, 20 Jun 2024 23:59:14 GMT  
		Size: 2.0 MB (2010468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40059883d048c029769e02acf2edd2df97523b78b5e0df01ae761d39c3d1ca8`  
		Last Modified: Thu, 20 Jun 2024 23:59:14 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0eef4938cb690c252242994fd1be404d38f0a2c5cee7d4231b1662ecadddd78`  
		Last Modified: Thu, 20 Jun 2024 23:59:15 GMT  
		Size: 18.1 MB (18054144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d3a0ac7415204d6e196e20be8a9554ae1efff6ea84c56b28e12d65578427c3`  
		Last Modified: Thu, 20 Jun 2024 23:59:15 GMT  
		Size: 18.2 MB (18178853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fc9b45b17bce32a551324bfa1a4cefb6f4ff1ca57aa78f1d3663948855ed70`  
		Last Modified: Thu, 20 Jun 2024 23:59:15 GMT  
		Size: 18.8 MB (18770948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcf5ea44c05ff53bb66e37863eca61b6b3bd0c0c81a52a585ed5697e5b176c8`  
		Last Modified: Thu, 20 Jun 2024 23:59:16 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219e595ad0a8708b5326afcd45023a57f60b288767bfdd637c9d985a37831d8f`  
		Last Modified: Thu, 20 Jun 2024 23:59:16 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2986c95c7e5a32cbcd88242d6150456a6f74921824aff8659834d5e67a92e907`  
		Last Modified: Thu, 20 Jun 2024 23:59:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921c0a0c766d1bda0faac83ff899ce8931cd081df604c9ffd49cb32a4439708b`  
		Last Modified: Fri, 21 Jun 2024 01:02:41 GMT  
		Size: 12.5 MB (12504327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38376a05507769d1f0769e335200562e5d978455a8ebe12c2472f77fc51cff9a`  
		Last Modified: Fri, 21 Jun 2024 01:02:41 GMT  
		Size: 89.2 KB (89187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5791e1a08695df4f87a4a4a3769bfd8bc3e303d7d06a140aedb5ed45739d9e45`  
		Last Modified: Fri, 21 Jun 2024 01:02:41 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a765629918b662166e5d4facda67b5e01fbe0aa27fc7465a605dea854b42c1`  
		Last Modified: Fri, 21 Jun 2024 01:02:42 GMT  
		Size: 56.7 MB (56713272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c748af66c987704c6616378f0c7603376d1e5d40e8455416bddf5e393f822b`  
		Last Modified: Fri, 21 Jun 2024 01:02:42 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d6e0e268570d9aca58a1ff1ed4f11d90197904437a5f4896364e4e12305d3e`  
		Last Modified: Fri, 21 Jun 2024 01:02:42 GMT  
		Size: 3.3 KB (3253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ddbd82245cc5879e920f89668026daeedf7e2367708ca652e7a4feda4472f4`  
		Last Modified: Fri, 21 Jun 2024 01:59:20 GMT  
		Size: 981.0 KB (980958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c9d4d61ae0ba258716bebc04c31d40b17dbcbc3a8c534c17afbe655007b345`  
		Last Modified: Fri, 21 Jun 2024 01:59:19 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933706d4c0609b47b97de886817cadf8f74f64e2ef85539e18ef1d5e15c52519`  
		Last Modified: Fri, 21 Jun 2024 01:59:19 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da25e7362e4a2357e0760961460b5681b5aeccb6fc9d0780b497876a06926116`  
		Last Modified: Fri, 21 Jun 2024 01:59:20 GMT  
		Size: 21.0 MB (20982367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c7ec23b67dcbe0db89cfdee60fb420ad635ed0b85648fe415559d4be77557e`  
		Last Modified: Fri, 21 Jun 2024 01:59:20 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:0be29b3152ddbe30a5da6a2f39ac6c4e29d4f71274da720951a889d4fcd76c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c6ca4cc605dcd8ca7be5d8df5a7a7b2586cd80d05f129684aedf4064ce2ffb`

```dockerfile
```

-	Layers:
	-	`sha256:7cea3a633acf2fff75cd97b6c4ea6a24dc33f0d03a8d7376f7f50ecb88e127a3`  
		Last Modified: Fri, 21 Jun 2024 01:59:19 GMT  
		Size: 30.6 KB (30586 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:26-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:fbfbf090c068128bd516a14294a3736a8bf2f4163e88c01d59341c088bc1e2c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146060629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7fed23787cd8f18b0e9d1cc216758ad5d8d8a81c63f239751b9be58cb3341e7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Wed, 05 Jun 2024 18:50:46 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Wed, 05 Jun 2024 18:50:46 GMT
CMD ["/bin/sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_VERSION=26.1.4
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.2
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-x86_64'; 			sha256='6fbaf6e93ccc43078a71a12db1d38224725cb5a9675391c38510355073f24066'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-armv6'; 			sha256='10b465c1771c262d372e24b09ed30fdc63687e35ae61c2365089e3998372a776'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-armv7'; 			sha256='b5bd40dfadf089617fe9cacb7a08d6fd5fae28e2a465191be1f25f22ffead344'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-aarch64'; 			sha256='de8c48203f4876fe3ae8bf27081a9aa69dc87de67a705f9d76c3a3ad776ed0c2'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-ppc64le'; 			sha256='5810b3e6184032edbd21f12ed165ddecc823b8222ff5e4f6c55112af6f617c6d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-riscv64'; 			sha256='2c138daa9eaa909434c808018c4ab748a5f25caee16e3a7810fbeb3897b40878'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-linux-s390x'; 			sha256='4084bdab8782e98c57a5f7aa7384699490048ce117dc7e70cad183702cc1645b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 05 Jun 2024 18:50:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
CMD ["sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-26.1.4.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-26.1.4.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-26.1.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-26.1.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
VOLUME [/var/lib/docker]
# Wed, 05 Jun 2024 18:50:46 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 05 Jun 2024 18:50:46 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 05 Jun 2024 18:50:46 GMT
CMD []
# Wed, 05 Jun 2024 18:50:46 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-26.1.4.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-26.1.4.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 05 Jun 2024 18:50:46 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 05 Jun 2024 18:50:46 GMT
USER rootless
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe01b594f40bdec3ca33c28b35f6c07fdcab95fbd6b3dde4e5a726487139f99`  
		Last Modified: Fri, 21 Jun 2024 07:16:21 GMT  
		Size: 2.0 MB (2006605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c80050ca831a092bdc48b735d815a7ea2c5282900d0ae45b061524c464cf1d9`  
		Last Modified: Fri, 21 Jun 2024 07:16:21 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069981f0e9920d2d495387512dfd06ee0cfbe9805545d42f7832e816f452f5da`  
		Last Modified: Fri, 21 Jun 2024 07:16:47 GMT  
		Size: 17.0 MB (17011541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca874a26f2ca26db5a16810720a18782d6c6c742f4b389fa1cb32e436bda590`  
		Last Modified: Fri, 21 Jun 2024 07:16:47 GMT  
		Size: 16.5 MB (16538046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22a55d54f75a11199433d3573f2efdf246b42b22d4d647b58a1d6957ca20722`  
		Last Modified: Fri, 21 Jun 2024 07:16:47 GMT  
		Size: 17.1 MB (17137930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0ecb2dd08f5d1d52cb6f63ec19b5d5e8979c209c2f40033bca4887a4c3af65`  
		Last Modified: Fri, 21 Jun 2024 07:16:46 GMT  
		Size: 545.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1950211de6f8c1e495630d2c2b93ddd933ac7317b9aef9766a65f6dce79a01`  
		Last Modified: Fri, 21 Jun 2024 07:16:47 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396b4022507da38e282b69c831f78dcbd216e355ad41973ef3e5eac1435da1b4`  
		Last Modified: Fri, 21 Jun 2024 07:16:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72352bda536e44bccefe58c6c218e2f79e2bab8b2a4b551fa14c23b8121c0b2c`  
		Last Modified: Fri, 21 Jun 2024 15:52:54 GMT  
		Size: 13.0 MB (12991087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd0e487498bf4679e6bb0dfc4b30981c4983e5ed85f75f1b69912f2c245338d`  
		Last Modified: Fri, 21 Jun 2024 15:52:53 GMT  
		Size: 98.6 KB (98625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2cbecde198a2fdd14e7ae17b114462fd6564e086b92d0e28e66b067a1d58da9`  
		Last Modified: Fri, 21 Jun 2024 15:52:53 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4019d9564051f13e7d62a692f895c9785d2547680418bf94afdb76957cf19d`  
		Last Modified: Fri, 21 Jun 2024 15:52:55 GMT  
		Size: 52.3 MB (52318653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b805aa8c77759725cafd6950eca8a7acc0094121b1cf92e3152fe8857b284b`  
		Last Modified: Fri, 21 Jun 2024 15:52:54 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bc67d40e248766c4640e5a69783e3d76dc2bb354f94f5afa0c337428c52b59`  
		Last Modified: Fri, 21 Jun 2024 15:52:55 GMT  
		Size: 3.3 KB (3252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281e15999bc228da4e57907b7f6dc69bb89a7a3c18d2786fc321b4f83bec6ddb`  
		Last Modified: Fri, 21 Jun 2024 18:51:53 GMT  
		Size: 1.0 MB (1023087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef25d6eb61cff5514d3a90f75753bc3a9de65e2490add13d4635664d5cd0065c`  
		Last Modified: Fri, 21 Jun 2024 18:51:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdafcd234e8826c6b96fe852ab9d01f97314aaba039cfb4b0ab58c2b8bd08aa3`  
		Last Modified: Fri, 21 Jun 2024 18:51:52 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b5b9b6f0e90b6b86cdc50a631c75c68b2faac41ccad06e9797f5b21a5361ec`  
		Last Modified: Fri, 21 Jun 2024 18:52:06 GMT  
		Size: 22.8 MB (22836951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4e8fd91cf9f2494a2a28952bda425a511b0bc243426a98593a6b70e1a785b7`  
		Last Modified: Fri, 21 Jun 2024 18:51:53 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:26-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c1d10d40c6a291dbbe9ceb92c0f257b16567b6bcfd90c38f03147add3cf28c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (31012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3176b94da50659b7befda4e7bc0000dfd85e2ecf97e0b84f169b1f80e7d5c567`

```dockerfile
```

-	Layers:
	-	`sha256:adc42451a375c1001a839369e3121c29a80e2756addc0341157246aa6a64ac46`  
		Last Modified: Fri, 21 Jun 2024 18:51:50 GMT  
		Size: 31.0 KB (31012 bytes)  
		MIME: application/vnd.in-toto+json
