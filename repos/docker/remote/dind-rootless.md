## `docker:dind-rootless`

```console
$ docker pull docker@sha256:8853961164089ed6f6751ea8002a93b0c633c824b017a7e311f66161d4717c37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:609c032e4f19010d6cf2aa7c39b3edb81925c7def4db821b30c9ac01210ff279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144631383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:685fa4f44310603802bf4fe41c9e2892522241fb24356cae2d679361608eeca6`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2024 12:05:09 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
ENV DOCKER_VERSION=25.0.1
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.3
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-x86_64'; 			sha256='49b3b71e4428585f75294a83702d259f442a8fcdb2351864c6dcaa3f7e29b3aa'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-armv6'; 			sha256='20cf111b8f28dc0e5b390ef6685c5504fc243597737ca46dac27e19e3f34190d'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-armv7'; 			sha256='d08bc3066c07effc6e7115197ce410d16c6c0974d5a746f0c6d02bc4c10b8348'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-aarch64'; 			sha256='c5a2bdf09db39c2aaf820ed9d6bab0ee9de187411ab37b869a7df20d3dbbceed'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-ppc64le'; 			sha256='e7e39ebbc2c42d17d5e6a2938f3ed9c5989380d569b84bbcc916000ec276527d'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-riscv64'; 			sha256='5b9a52806b8363d170770548ca7baf25c1f96dca1da837265b2a42989c323e32'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-linux-s390x'; 			sha256='258e548656bbce1a44459fcf579927b59a17b284e730d680843c19a699bf7739'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 24 Jan 2024 12:05:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jan 2024 12:05:09 GMT
CMD ["sh"]
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
VOLUME [/var/lib/docker]
# Wed, 24 Jan 2024 12:05:09 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Wed, 24 Jan 2024 12:05:09 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Wed, 24 Jan 2024 12:05:09 GMT
CMD []
# Wed, 24 Jan 2024 12:05:09 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-25.0.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-25.0.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Wed, 24 Jan 2024 12:05:09 GMT
VOLUME [/home/rootless/.local/share/docker]
# Wed, 24 Jan 2024 12:05:09 GMT
USER rootless
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e220044d47fac30433397406bf22928e34b2c5128a81bad384de4fb60cca96d`  
		Last Modified: Wed, 24 Jan 2024 20:49:44 GMT  
		Size: 2.0 MB (2018470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa8dbba8092ecc789f7e71231376e065be317a6fd76bb62f97598665d86ae54`  
		Last Modified: Wed, 24 Jan 2024 20:49:44 GMT  
		Size: 549.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3fe3c8403258f4e603ef6b9c6c296381ee65b339f445fe457ff07097a57386`  
		Last Modified: Wed, 24 Jan 2024 20:49:45 GMT  
		Size: 16.9 MB (16894262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60b56d14d45dd09ec955b54a891bd01f10ca6bc995c26442bddb787012812d3`  
		Last Modified: Wed, 24 Jan 2024 20:49:45 GMT  
		Size: 17.2 MB (17195299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6ffc0cc1bbfd610a27b0956a703228ac76f32bb9b42773af7c16db672196f8`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 18.2 MB (18175344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884c38f9f4c343719508697b84f52abf0b70989d1628063ebe057a603537b8d4`  
		Last Modified: Wed, 24 Jan 2024 20:49:45 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110f5ca54c61635c027ed0bad8c095b040c9555207f6bcad1f23538e1b3ff48f`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a890c86f6be5c8a68116c474ce792f5ef84cfa070aa75eed8c969e97dcb5221`  
		Last Modified: Wed, 24 Jan 2024 20:49:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db61228bc45945df235a4f738274d46b0cd326426a4d731a43bde6b3e9e264b1`  
		Last Modified: Wed, 24 Jan 2024 21:49:36 GMT  
		Size: 9.3 MB (9258191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315081ca3661803493e78b59274e9f46cd37f3cb02fc4362f40306972fd2a82e`  
		Last Modified: Wed, 24 Jan 2024 21:49:35 GMT  
		Size: 83.6 KB (83642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ccda2fad9a7e8b73e58f883b2d60c0738c0facc77076b30964e3619977a2ad`  
		Last Modified: Wed, 24 Jan 2024 21:49:35 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:facdb98f28a710ef33eb3c82cc1b97aedf5550bd7bd79af1bace19910f224c2a`  
		Last Modified: Wed, 24 Jan 2024 21:49:37 GMT  
		Size: 55.6 MB (55635195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bae1cc52784fa09c34ab5e76e18cb3001f4b38669a49babd5aec4592286053`  
		Last Modified: Wed, 24 Jan 2024 21:49:36 GMT  
		Size: 1.5 KB (1510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808a2e4f73b4b856452e9ea92039092a01002fdd74a6017a7eeabf2c040011a5`  
		Last Modified: Wed, 24 Jan 2024 21:49:36 GMT  
		Size: 3.2 KB (3249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd4ec505ee2bd6196e137b7b3b0f86e98a87959200ea8bbee14faa343533c9f`  
		Last Modified: Wed, 24 Jan 2024 22:49:54 GMT  
		Size: 974.0 KB (974050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f5996f38a3b5dea4b2b820fc464539a959141ea60793a78656c1181564b31d`  
		Last Modified: Wed, 24 Jan 2024 22:49:54 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae74ba3705629f50b5c309805708bbec3a99d47df23fdd98d954593a235cca1`  
		Last Modified: Wed, 24 Jan 2024 22:49:54 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e7523595e95c922e27143b1aa67bf9a288982908be77bf9aee83c98a31450c`  
		Last Modified: Wed, 24 Jan 2024 22:49:55 GMT  
		Size: 21.0 MB (20978490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:facf351fc0108d529141b0110658a8a2f4ec9c8570d6b67c3e8eeca7244251d2`  
		Last Modified: Wed, 24 Jan 2024 22:49:56 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:209afd2c65329307c27254c926abefdd978ae38dbeaeac9abdcba8996ffe6774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **769.8 KB (769757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caec9c021d294718f1dab777910bfa3b70633ecdb746c829c68009685181fba3`

```dockerfile
```

-	Layers:
	-	`sha256:816530b05ccc44678c89f8d075a3e49479c1be4dfb9b2578d62189d1c3f00487`  
		Last Modified: Wed, 24 Jan 2024 22:49:54 GMT  
		Size: 736.5 KB (736508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:840d3d403c6ee32cca95f316148035e18c1f1bd7d8df8d36167f08a1dc083aa1`  
		Last Modified: Wed, 24 Jan 2024 22:49:54 GMT  
		Size: 33.2 KB (33249 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:963e027db24cdf5664801b06a9d169ad4213008d713582deade629e9c7643916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138317070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a12fbab545fdd22e0c3d6f789b750413cae82aeef2d99bf73e7b7f376bd142`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Fri, 19 Jan 2024 12:04:26 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
ENV DOCKER_VERSION=25.0.0
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-amd64'; 			sha256='716321df8ca9c82ffe96f37e9f4aa1199d4969795836dbd57ef72d12e3ac5085'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v6'; 			sha256='4b3c78b59c0383ab21327e2902af2ea317e3b85e442b1cd776f0c2a7bbbb2999'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm-v7'; 			sha256='fe0a9e7812051a72c47d009bf9373e76e23644cc3291c848ac4a9b6f237e9e75'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-arm64'; 			sha256='fb72d627f2ee080bba70375c367f4292867821e29ca9a8cf485622f6ede8f436'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-ppc64le'; 			sha256='1c649498d727183d82fb243e08856533ea90e8d63bfcd6f8b23b264dbcf7ea7a'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-riscv64'; 			sha256='152e7b423c1ce888eb0a658321eb8c28cc1d09af01acd5c66eddf8474dddf55c'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.linux-s390x'; 			sha256='acee98a9f0550bf2c6c1161cf8067c031ddf0c566c41de7db27847bb72e8ee0b'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.2
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-x86_64'; 			sha256='067a12983b9333d01947329190af756b6d12afe7b4b51b3e1e29328b4afe3b9f'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-armv6'; 			sha256='582d734ef0c14335ee4691f3550d56b3e1c1c4d787ed6354830b3c222eee542e'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-armv7'; 			sha256='e83fa84dc73cc8d5a0fe2d1ad3ad61202050f033e6df9f3f4f7b3c2b59181006'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-aarch64'; 			sha256='beafe762fedd06fe9885317c33f8b29b39c2354d6840a494a69b3c3a36919212'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-ppc64le'; 			sha256='6be73d6597efc822eff3f9dd6abb56b72ada76f8a5f798b1df2dce5105f39257'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-riscv64'; 			sha256='33a15fcef9d975aee4ed404779fae068264da6de8f2851ead85f9e1701302411'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-linux-s390x'; 			sha256='0b62a8d7aad7ce81220a4d77aa4b17e443b888248c1da22bc808db1fcbf1e9ac'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 19 Jan 2024 12:04:26 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jan 2024 12:04:26 GMT
CMD ["sh"]
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-25.0.0.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-25.0.0.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-25.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-25.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
VOLUME [/var/lib/docker]
# Fri, 19 Jan 2024 12:04:26 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 19 Jan 2024 12:04:26 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 19 Jan 2024 12:04:26 GMT
CMD []
# Fri, 19 Jan 2024 12:04:26 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-25.0.0.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-25.0.0.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 19 Jan 2024 12:04:26 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 19 Jan 2024 12:04:26 GMT
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
	-	`sha256:594895876a66f55998b0c3d9c175ec0cfa723898879d7fe8f837de3b0e9e01e6`  
		Last Modified: Fri, 19 Jan 2024 20:23:15 GMT  
		Size: 15.9 MB (15901598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5598890badaf41ad29ca6e7a62aecf9b18e64ff1308118644d6ecda191bee6ae`  
		Last Modified: Fri, 19 Jan 2024 20:23:14 GMT  
		Size: 15.6 MB (15640596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08400fbc822ec742c74feaa2c8ada0afc029515edf89fec4102a3aa26dae8a3`  
		Last Modified: Tue, 23 Jan 2024 01:47:07 GMT  
		Size: 16.6 MB (16607523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb634b0bcb9abfaa96af63dbdfd8e366dc9b1fbe0de8b906c4d9d312e5f90418`  
		Last Modified: Tue, 23 Jan 2024 01:47:06 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7303addcbef4ecd329f524a7931a7c0856d5c284f751716ef9934dff4462b8ac`  
		Last Modified: Tue, 23 Jan 2024 01:47:06 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc13d7fb096bafcb15abbc0caa3609ccd8976bd665c9d1b526968be6a672c0e`  
		Last Modified: Tue, 23 Jan 2024 01:47:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0362c233aa96b1b25f85d331f1f6d7398b55eb9950ad741c7d9bbc5b98ba4f4`  
		Last Modified: Tue, 23 Jan 2024 03:40:25 GMT  
		Size: 9.5 MB (9509900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dbaf54b8a1056063c003d28c07f7f0de04270e356dc6b97bf65b5ca80f3e89`  
		Last Modified: Tue, 23 Jan 2024 03:40:24 GMT  
		Size: 93.1 KB (93073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c586bb90165a8329810aa5de6d6f91ade04d5ce4db75a02707c8e7ecb1c2196c`  
		Last Modified: Tue, 23 Jan 2024 03:40:24 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88199d360a37daa0821830ec4572d6f6cf61b6c4b1b7b2517b4f0fcf72985c91`  
		Last Modified: Tue, 23 Jan 2024 03:40:26 GMT  
		Size: 51.3 MB (51341152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33a9603a501d05c28d09912ec599b5dd2576f565e587ad1ebbb19424bc9066e`  
		Last Modified: Tue, 23 Jan 2024 03:40:25 GMT  
		Size: 1.5 KB (1506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53b81318cb74f48833fe965ede341742c760668ddc1baa655b1c1f8f7f5291`  
		Last Modified: Tue, 23 Jan 2024 03:40:26 GMT  
		Size: 3.2 KB (3247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e873e196f6a4baa6ef58b71732828e01d0bd2a04f172b7e67a85f7fe422c2f4`  
		Last Modified: Tue, 23 Jan 2024 04:29:38 GMT  
		Size: 1.0 MB (1016252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f3eea6930a240ff1955971b48c710ca07f7f9d9a4ee78f71352a879c84ee82`  
		Last Modified: Tue, 23 Jan 2024 04:29:38 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd8ee617d9e642b2cdeb1893e31995212e697e17aa7dca2ddd6a49c4d6eaf79`  
		Last Modified: Tue, 23 Jan 2024 04:29:38 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7dd34c1cabdfd0ea045b6d03c73eb561a0ba724ed735b2d540c449fe6f3e326`  
		Last Modified: Tue, 23 Jan 2024 04:29:39 GMT  
		Size: 22.8 MB (22834326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6413fae6f24274401981923d3324fa0c2eb9dfa45aafd0bb04b01dbd21e0e5c`  
		Last Modified: Tue, 23 Jan 2024 04:29:39 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:d8f91f339f5cfc65388ead0d7c6fd4178a644e3cc2b67b4d56f0a1f99017b617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **769.8 KB (769832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:450365ae4808345b55eff9ca00a3f71442c10d3388756d89bddf1db49463fa32`

```dockerfile
```

-	Layers:
	-	`sha256:23b6c157800adce5b03168f4c9b1d5bffb027d57e3c4104ee9166647c0db0ccb`  
		Last Modified: Tue, 23 Jan 2024 04:29:37 GMT  
		Size: 736.5 KB (736520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7839c6186e6e5ce6be537d630a3637afd9775020cc35e1b2d7a5067ab5f033ef`  
		Last Modified: Tue, 23 Jan 2024 04:29:37 GMT  
		Size: 33.3 KB (33312 bytes)  
		MIME: application/vnd.in-toto+json
