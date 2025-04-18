## `docker:28-dind-rootless`

```console
$ docker pull docker@sha256:eb151b0f024b9d46ecd6eeafb45ea85ff87855c1129ad3c6bc7daac1de5d100f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:28-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:61b88b38f34af132b0ed428307b1a85a7dbb905804c91e70e050ad91eaaf3060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (159033978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5791efc10f047744d4c4956d07cd692b7087ac185f2bed7ca7f535c67f75b21f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_VERSION=28.1.1
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-x86_64'; 			sha256='7bdb2ce2916e5dd0354e5d129892bf96fdcdb1a9ab8eed69b9173e131db4c230'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-armv6'; 			sha256='dc555cf80a1c5849853a71083f4930790e6515d14c31060de77e6d83bbc996c3'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-armv7'; 			sha256='50aba1c8fe1eb8efefede3dab9e6c2226ba756a5ffa5cf4f4f5baadaee9a7455'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-aarch64'; 			sha256='a91e930a076b91e6c69f11d1dbe3c06729ae765fb9dbb3f97cb808e784647399'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-ppc64le'; 			sha256='fa6b67a69916a99d14191df5dee1e8399d5eb07f1d322f04caa2078045cb0140'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-riscv64'; 			sha256='c582635c0c4fb1e692dd8a7de206373866f2aa3fcfd9cf03d2358585e602e15d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-s390x'; 			sha256='8cb63254106ceded2373a86355f48ea410564e748521a4b097e3d43b93c05e24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 18 Apr 2025 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
CMD ["sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
VOLUME [/var/lib/docker]
# Fri, 18 Apr 2025 17:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 18 Apr 2025 17:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
CMD []
# Fri, 18 Apr 2025 17:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 18 Apr 2025 17:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3b451c4c6d32883a5f72f81984b664a7fe95fc155d0e1f2853024c83a58670`  
		Last Modified: Fri, 18 Apr 2025 18:17:40 GMT  
		Size: 8.1 MB (8062915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b64f750a09224d0870be8b95c1f8c0f5da14242d6c347c9db061c8a49d4aad3`  
		Last Modified: Fri, 18 Apr 2025 18:17:40 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e19e08b20db35f12c452a9f931ab62834b628e5d2a856c6f4c41fdb9f3bd208`  
		Last Modified: Fri, 18 Apr 2025 18:17:41 GMT  
		Size: 19.6 MB (19565537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ff937cfa7898506265b9be2e80af177cea5a50c9fe07ac950f350c2650dc56`  
		Last Modified: Fri, 18 Apr 2025 18:17:41 GMT  
		Size: 21.5 MB (21456664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53278fe5e6f0a18c6876daa2e23f0eaffdaf92e59c4d03a2319c02ff17b521f`  
		Last Modified: Fri, 18 Apr 2025 18:17:41 GMT  
		Size: 20.9 MB (20923468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e060defd84a5b8b5d299d3e901fc815cfd866c50bec5774d2dcfb74bc6c5289`  
		Last Modified: Fri, 18 Apr 2025 18:17:42 GMT  
		Size: 536.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63dbc57c1a2a16e5625f4665821afe3d557ec311502a001fbb1ccb991b9e08fb`  
		Last Modified: Fri, 18 Apr 2025 18:17:42 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1293ab979e28ba180d1e00bafe3f48454e67eab044b1d4474a570137c4f84bb3`  
		Last Modified: Fri, 18 Apr 2025 18:17:42 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a4127e99cf00b776cd7bb221563f1741b31821a920810bbaab59f1cebae368`  
		Last Modified: Fri, 18 Apr 2025 18:37:28 GMT  
		Size: 6.7 MB (6732965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f418ff940aa354e9998da6a6faa66937d877c2b84ef0ba8b3aa70396cbc2ccd5`  
		Last Modified: Fri, 18 Apr 2025 18:37:28 GMT  
		Size: 90.3 KB (90337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d0fb59c4c5184b7426f477543d268d0d8ef9827fba5da1ed40160d4151267d`  
		Last Modified: Fri, 18 Apr 2025 18:37:28 GMT  
		Size: 1.0 KB (1013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6535ddaccd53733ead4324794f18cfd8d8d53e7af84d295fceb51f9be414d0`  
		Last Modified: Fri, 18 Apr 2025 18:37:30 GMT  
		Size: 60.4 MB (60382736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8d00d6e5e80757d1a19f4945f84bede6356c9ec3f1cd1778c3a7fddd557e57`  
		Last Modified: Fri, 18 Apr 2025 18:37:29 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfabfe011b48f229a29bb05f4fab34b929eed0c9519723f469fb0ca12319a079`  
		Last Modified: Fri, 18 Apr 2025 18:37:29 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbab2106cc924c1f80c9fb3722421b3fccff7eeb76a1d3ef8180645af561ebc6`  
		Last Modified: Fri, 18 Apr 2025 19:07:48 GMT  
		Size: 986.6 KB (986578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d60cdea8edbd8a92127465475dc203ce39decd25a19b1037d56b3fc137999a`  
		Last Modified: Fri, 18 Apr 2025 19:07:47 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d010ff684e47f35834b04249db1970bd145eb4bad09ad4f2db530dd73e1968e`  
		Last Modified: Fri, 18 Apr 2025 19:07:47 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20244245ae21471f25a360de84296548083559a94e898e0d340a3924572b2434`  
		Last Modified: Fri, 18 Apr 2025 19:07:48 GMT  
		Size: 17.2 MB (17181085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff10e628a6704f0ea7b438852e354b73b639a599d2f66496a10ebe38a495cdd`  
		Last Modified: Fri, 18 Apr 2025 19:07:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:b3913d6ae55a9365dad6134b1f7511f2628cbe63bdcd49bfdf5cc35e89e44e3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63d622aa06536fadc97c9b9c707cbd70d69514a2df341ec6cb30107583ba714`

```dockerfile
```

-	Layers:
	-	`sha256:fe0fc98589806465160b1ec10fad42200a441d544d998ad9b00d31c3479baa31`  
		Last Modified: Fri, 18 Apr 2025 19:07:47 GMT  
		Size: 30.5 KB (30452 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:28-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:18ee049f92af8f48a082486f69cc654f8434fe01317cddb2a0911f27b3b70e9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152550237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50694562236510daec41d5acd8468ec2c134dd4703cf9035408f8fde046f1217`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client 		git # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_VERSION=28.1.1
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-amd64'; 			sha256='55838fdd095084e158e06a63635a07fe8a8bc6cb4db507f203394dc1ffa7fb8b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v6'; 			sha256='0a74f020bf67c22b8564c93ac84b393cc8c3d319fc210779dfe9b2594422a5e9'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm-v7'; 			sha256='3ab9d3838aedce5ec6ecaecb85e664689d57292d19a6ddca9fb31f0950259ce6'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-arm64'; 			sha256='50b0b14770127b292e3e2f756d0137152b08afc1d7daa09f49d2b6e6fa1b1b81'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-ppc64le'; 			sha256='d7251d345225a7ab908b96010447d98767174ded277979cc10280ba1d31d8cf6'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-riscv64'; 			sha256='3c225413839ec1bd84a0fdc21614046e4fdaa2afe6bbb9057c75a024f520d5a8'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.linux-s390x'; 			sha256='e4a662893ac1983b1298569959b2e2c4b9dcf6c9d589fb00997926971853c717'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-x86_64'; 			sha256='7bdb2ce2916e5dd0354e5d129892bf96fdcdb1a9ab8eed69b9173e131db4c230'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-armv6'; 			sha256='dc555cf80a1c5849853a71083f4930790e6515d14c31060de77e6d83bbc996c3'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-armv7'; 			sha256='50aba1c8fe1eb8efefede3dab9e6c2226ba756a5ffa5cf4f4f5baadaee9a7455'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-aarch64'; 			sha256='a91e930a076b91e6c69f11d1dbe3c06729ae765fb9dbb3f97cb808e784647399'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-ppc64le'; 			sha256='fa6b67a69916a99d14191df5dee1e8399d5eb07f1d322f04caa2078045cb0140'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-riscv64'; 			sha256='c582635c0c4fb1e692dd8a7de206373866f2aa3fcfd9cf03d2358585e602e15d'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-linux-s390x'; 			sha256='8cb63254106ceded2373a86355f48ea410564e748521a4b097e3d43b93c05e24'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 18 Apr 2025 17:04:15 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
CMD ["sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="$(command -v "${f/tables/tables-legacy}")"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-28.1.1.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-28.1.1.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
ENV DIND_COMMIT=8d9e3502aba39127e4d12196dae16d306f76993d
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
VOLUME [/var/lib/docker]
# Fri, 18 Apr 2025 17:04:15 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Fri, 18 Apr 2025 17:04:15 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 18 Apr 2025 17:04:15 GMT
CMD []
# Fri, 18 Apr 2025 17:04:15 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-28.1.1.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-28.1.1.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Fri, 18 Apr 2025 17:04:15 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 18 Apr 2025 17:04:15 GMT
USER rootless
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e908642e05b5fbf003c9e4a8221bae6272e763cdb2b4bfc1b5e8b4390cf6fe26`  
		Last Modified: Fri, 18 Apr 2025 18:18:42 GMT  
		Size: 8.1 MB (8077213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921ebed4db9f28c529f50025fce538c298774c7875dd8ddad6ed2013a5aa6792`  
		Last Modified: Fri, 18 Apr 2025 18:18:41 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e39b077a4cb6428bb4da55a189eada7398a9f694e967b97325a6ab7b090604`  
		Last Modified: Fri, 18 Apr 2025 18:18:42 GMT  
		Size: 18.5 MB (18485739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a55093f87621ee6c799416e629871a8fc094b95c6ac81c19dfd11f5e93af516`  
		Last Modified: Fri, 18 Apr 2025 18:18:43 GMT  
		Size: 19.7 MB (19692479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4a4a535b8c9b4c9ad9ef6731c67cb4003609d3ca4a2b0804651dffcf0f239d`  
		Last Modified: Fri, 18 Apr 2025 18:18:44 GMT  
		Size: 19.2 MB (19183026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa4121a3e10341b36d1150ea60b95ca22b252f073074f4579162fd3de89a77f`  
		Last Modified: Fri, 18 Apr 2025 18:18:43 GMT  
		Size: 534.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d159dcc3a2ada658492f3f5415a04a24ddd863055ff5f6e4b5d59c845821bdd`  
		Last Modified: Fri, 18 Apr 2025 18:18:44 GMT  
		Size: 1.0 KB (1007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c2b2213d30786df315c412e43f3b191cc2c39ae5659a881e48b6088d968518`  
		Last Modified: Fri, 18 Apr 2025 18:18:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988965604792fd3fdb08d948778bd4576e27ecd67b8f8dd3483c1b6fbe20f081`  
		Last Modified: Fri, 18 Apr 2025 18:36:42 GMT  
		Size: 7.0 MB (6978881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76eefe96f3a7cf3f7ce95ec40e54098f44d4ffe32e37157ece57e7e9351a5f9`  
		Last Modified: Fri, 18 Apr 2025 18:36:42 GMT  
		Size: 99.4 KB (99393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78bf806e19afb9c609956356f28d880e4bb4cc87e3c9d5a98f59ccaeb944f5b2`  
		Last Modified: Fri, 18 Apr 2025 18:36:41 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5378ef72691336a01721dc4a8c48bb48b49c2fca2a0685636b3adeb211767d0e`  
		Last Modified: Fri, 18 Apr 2025 18:36:44 GMT  
		Size: 55.7 MB (55741017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f09d35ff6682c3f813ff00012378b62e573c35f57b9efa8793810a5aa993627`  
		Last Modified: Fri, 18 Apr 2025 18:36:42 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ad1a9ed82ecb1314f380750d4a08831e3a3e91596e5660f922aad0a42cc43b`  
		Last Modified: Fri, 18 Apr 2025 18:36:43 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5960424a2d35106c06a33e99b596768c2b0758398a80a31c0d422d8d947e3838`  
		Last Modified: Fri, 18 Apr 2025 19:07:19 GMT  
		Size: 1.0 MB (1014219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618a15814ac35f0a120f1643f496c8702934efffc53a5b71e2826cb39b102c0a`  
		Last Modified: Fri, 18 Apr 2025 19:07:19 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27311ae1d14bbcee3875c2051b64fbd7c71669ac7d630db4ce9e6ba63586ae46`  
		Last Modified: Fri, 18 Apr 2025 19:07:19 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a0fe960ac1e8ee2d2b33f8d5fa06c1fbb2894d271568a688770feb23f3f810`  
		Last Modified: Fri, 18 Apr 2025 19:07:20 GMT  
		Size: 19.3 MB (19275803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa8dc67f13ccb5a4c04ab1cfc5b992b19a9f73d46e88612eed37fda0b45541c`  
		Last Modified: Fri, 18 Apr 2025 19:07:20 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:28-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:c1421e1f8dfdc89edb842f7d5e6135f7283461880afefc74802f9a4b60acfe5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e8be6e0cc5c264111cdaa21e645bf7c262d90edb54a3a4f0430093436ed903`

```dockerfile
```

-	Layers:
	-	`sha256:e05e09f71339d1f1b094399f8cd964a7f7dabde670befdbe9a1a7bd45a8d48f1`  
		Last Modified: Fri, 18 Apr 2025 19:07:18 GMT  
		Size: 30.6 KB (30620 bytes)  
		MIME: application/vnd.in-toto+json
