## `docker:27-dind-rootless`

```console
$ docker pull docker@sha256:8e1ffc044c0b4f941bba491987437341ccaeecae588f32908fa6dd8370d7a182
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:27-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:65c94f17eaf3021b427a81fe8507fccfac8220035ed2fc12a58beadc64476462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154408014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11e934057f7fc98160e96a24e68410748b2f57d85cf162bb20bcbb83eff2850e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_VERSION=27.0.3
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-x86_64'; 			sha256='5b480d4f9e3517b375f0fbb781b39c63cec934f44b13c43b8f1d0f22bf6de8c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv6'; 			sha256='ff366f16854e8febcdce21b750f6462abdcaa16209be490feaa8c2dd88b7884c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv7'; 			sha256='d829c0d3f85885ee29fcaf19d2b6001215820ad874a0b9cdc3172965acb80c50'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-aarch64'; 			sha256='1ce6f9842b10ee5f61218a62f3acfc5839a31cd6daa6e87e926bef63dd9fee20'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-ppc64le'; 			sha256='c02e6b718e94df66cd0a53349d6487dbc6da99aa582c0b9906637964ecd9bd15'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-riscv64'; 			sha256='9d5d8033a8cf3deb05c7a9ee7cdf0086cc24a526fa9a10b4a778cc9124f5ef25'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-s390x'; 			sha256='c8ac20d8fac6d982a83e3b5bb34cda5ac326fbfde9b43c64a290258a1d7fbb38'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 01 Jul 2024 11:04:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
CMD ["sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
VOLUME [/var/lib/docker]
# Mon, 01 Jul 2024 11:04:46 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 01 Jul 2024 11:04:46 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
CMD []
# Mon, 01 Jul 2024 11:04:46 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 01 Jul 2024 11:04:46 GMT
USER rootless
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337b172a7c470ffdd333d735c45d7728164db077839e493e6bbd19ce2eca4230`  
		Last Modified: Tue, 02 Jul 2024 00:57:01 GMT  
		Size: 2.0 MB (2010472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d917b3449c2fcfd6192f75a8feac930d263b21eab11e309ee38dfe3ee032435d`  
		Last Modified: Tue, 02 Jul 2024 00:57:01 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4e19c7f6853e90536da0a370212dc4e5347c5efa915d4f503c6d2c30f50502`  
		Last Modified: Tue, 02 Jul 2024 00:57:02 GMT  
		Size: 18.1 MB (18069814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21be6ea5d6f334b6fe1c4b8d29fd4a6bd95b786c8238e475b0d0f1a75d2cf8c`  
		Last Modified: Tue, 02 Jul 2024 00:57:01 GMT  
		Size: 18.2 MB (18178851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6304ca1e2076d6291e70355ad39f5b63a5a9682cfc62312152adea50123192eb`  
		Last Modified: Tue, 02 Jul 2024 00:57:02 GMT  
		Size: 18.8 MB (18792461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69e773f08c2994a5997d847a869210a7c5c69b19c26ab1aa79ff83ad6c65758`  
		Last Modified: Tue, 02 Jul 2024 00:57:02 GMT  
		Size: 542.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb84f9b00ac59f7b5fe94490b091cc258548f0a417f767428c2996ced97cc42`  
		Last Modified: Tue, 02 Jul 2024 00:57:03 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a71205c786763c16f77d6a06edb03a4286bd1e4395d812c9a8f37586e97d26`  
		Last Modified: Tue, 02 Jul 2024 00:57:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9a384269473f1e7ab781a869e8e9c7563ac518f2a43867c9851fe7a702ae6d`  
		Last Modified: Tue, 02 Jul 2024 03:02:46 GMT  
		Size: 14.9 MB (14914213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee4b7ed48762a43ee6301be676de5886b18cc314cd4ed51eba1d6e8b83dfbc4`  
		Last Modified: Tue, 02 Jul 2024 03:02:45 GMT  
		Size: 89.2 KB (89191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130a7cf002164b9ec6ca7ccac9fedf7199295e1240f280815a496479c7d4579f`  
		Last Modified: Tue, 02 Jul 2024 03:02:46 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1991d750d62bfc74871a8f7fb59419d77f1a962b83f914373bb2fe1298ca57f6`  
		Last Modified: Tue, 02 Jul 2024 03:02:46 GMT  
		Size: 56.8 MB (56756523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a02f0ed53a5604d1c058948e1d06eebe64836b8cc82fc7f431bcfbc5589f89f`  
		Last Modified: Tue, 02 Jul 2024 03:02:46 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1875a26f11176b3920c70ecb648089254ac253628ced5f03c140c376d593ee52`  
		Last Modified: Tue, 02 Jul 2024 03:02:46 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499ab6987db78f1c07e36b662e7b8155a076204e026593136fbda24a1bc7e9ce`  
		Last Modified: Tue, 02 Jul 2024 04:09:55 GMT  
		Size: 981.0 KB (980962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6543cbd5bf3cfeb59dc71a688019b81c71a25933fa8f1adaed9ff082b691db1b`  
		Last Modified: Tue, 02 Jul 2024 04:09:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1893725b92ba604bcefd28669b8c2492309cfe11016ad7cfa6fc26c930f71f9`  
		Last Modified: Tue, 02 Jul 2024 04:09:55 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0c50e2c81c91ed7c3a4a200b576a64666e84146f8809d2942192f25ca8c8ce`  
		Last Modified: Tue, 02 Jul 2024 04:09:55 GMT  
		Size: 21.0 MB (20982379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e88ffbe756df6d8ead3e26813ce8341f4d6506dfcae827770d979d70eabc588`  
		Last Modified: Tue, 02 Jul 2024 04:09:55 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:8bd51bdba243119354ca6d6f1464233779a30a8f284f09fc3f77e8bc3e04b6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf723c1c5a4cf4c960de2f4ddc1ed4a30eca20b08e6cc48b89095f009202bf62`

```dockerfile
```

-	Layers:
	-	`sha256:19f0043e956e5338b15470a6de34a6daeacc50e9e3512d9f1bd0ed76da2b7f36`  
		Last Modified: Tue, 02 Jul 2024 04:09:54 GMT  
		Size: 30.6 KB (30586 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:27-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:f40384d18e1bc9ede0d2b95af18f969613d8fafcd0fb61efc2350bc8942c01d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (148974938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f962c11cb243e3eab4a7985ed99155b58a8eca80d3166241159b21456381bc57`
-	Entrypoint: `["dockerd-entrypoint.sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	addgroup -g 2375 -S docker # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_VERSION=27.0.3
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-amd64'; 			sha256='8d486f0088b7407a90ad675525ba4a17d0a537741b9b33fe3391a88cafa2dd0b'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v6'; 			sha256='b4d1c41605b50b5549f1464461cfa72d010106bfb4606b45cc776daab4c25d7d'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm-v7'; 			sha256='eabc32a4a86f943c3996eb2df5efd0d02d12603e356941ed46c132c64cbcbcdf'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-arm64'; 			sha256='13f4ffd2b6922e941d6b6a9faee73ec9b8cab5b309ef90dfadf48142c2a47f34'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-ppc64le'; 			sha256='6b41769526c9102d2352ed6900de33ee4be2eaf1927cfb216cc832c718e5c990'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-riscv64'; 			sha256='52f5a974d8d1eb88d1defe0da5173d39df3608e554c3dcd1d45bde77c3d697f3'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.linux-s390x'; 			sha256='689c88555c42708ac812e3063590f8681b675d7f2ca68c024299ec388963615d'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_COMPOSE_VERSION=2.28.1
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-x86_64'; 			sha256='5b480d4f9e3517b375f0fbb781b39c63cec934f44b13c43b8f1d0f22bf6de8c3'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv6'; 			sha256='ff366f16854e8febcdce21b750f6462abdcaa16209be490feaa8c2dd88b7884c'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-armv7'; 			sha256='d829c0d3f85885ee29fcaf19d2b6001215820ad874a0b9cdc3172965acb80c50'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-aarch64'; 			sha256='1ce6f9842b10ee5f61218a62f3acfc5839a31cd6daa6e87e926bef63dd9fee20'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-ppc64le'; 			sha256='c02e6b718e94df66cd0a53349d6487dbc6da99aa582c0b9906637964ecd9bd15'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-riscv64'; 			sha256='9d5d8033a8cf3deb05c7a9ee7cdf0086cc24a526fa9a10b4a778cc9124f5ef25'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.28.1/docker-compose-linux-s390x'; 			sha256='c8ac20d8fac6d982a83e3b5bb34cda5ac326fbfde9b43c64a290258a1d7fbb38'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Mon, 01 Jul 2024 11:04:46 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
CMD ["sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		git 		ip6tables 		iptables 		openssl 		pigz 		shadow-uidmap 		xfsprogs 		xz 		zfs 	; # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	apk add --no-cache iptables-legacy; 	mkdir -p /usr/local/sbin/.iptables-legacy; 	for f in 		iptables 		iptables-save 		iptables-restore 		ip6tables 		ip6tables-save 		ip6tables-restore 	; do 		b="/sbin/${f/tables/tables-legacy}"; 		"$b" --version; 		ln -svT "$b" "/usr/local/sbin/.iptables-legacy/$f"; 	done; 	export PATH="/usr/local/sbin/.iptables-legacy:$PATH"; 	iptables --version | grep legacy # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-27.0.3.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-27.0.3.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-27.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-27.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		--exclude 'docker/docker' 	; 	rm docker.tgz; 		dockerd --version; 	containerd --version; 	ctr --version; 	runc --version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
ENV DIND_COMMIT=65cfcc28ab37cb75e1560e4b4738719c07c6618e
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
COPY dockerd-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
VOLUME [/var/lib/docker]
# Mon, 01 Jul 2024 11:04:46 GMT
EXPOSE map[2375/tcp:{} 2376/tcp:{}]
# Mon, 01 Jul 2024 11:04:46 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Mon, 01 Jul 2024 11:04:46 GMT
CMD []
# Mon, 01 Jul 2024 11:04:46 GMT
RUN apk add --no-cache iproute2 fuse-overlayfs # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN mkdir /run/user && chmod 1777 /run/user # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-27.0.3.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-27.0.3.tgz'; 			;; 		*) echo >&2 "error: unsupported 'rootless.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'rootless.tgz' "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker # buildkit
# Mon, 01 Jul 2024 11:04:46 GMT
VOLUME [/home/rootless/.local/share/docker]
# Mon, 01 Jul 2024 11:04:46 GMT
USER rootless
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3b21a9b13e2731b55350810e8b6223212f693aa1f3e11f69753c64dd297990`  
		Last Modified: Tue, 02 Jul 2024 01:17:59 GMT  
		Size: 2.0 MB (2006717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586562bcc1cb152206d02749d23793efb9912bb282c92e595007278d9d6e2ccc`  
		Last Modified: Tue, 02 Jul 2024 01:17:59 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f18f513eb64fc868ed9232c9b292d123aacc7b06892dd0eb039e721e27a639`  
		Last Modified: Tue, 02 Jul 2024 01:18:00 GMT  
		Size: 17.0 MB (17028618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe274b42de9ce5cff78a1240ae0582bc7202c890df0ebc599580687110e9dfe5`  
		Last Modified: Tue, 02 Jul 2024 01:18:00 GMT  
		Size: 16.5 MB (16538044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab320534093924fb46c1e4e1b3348fb9390c50fcffd47adbc32373e710ac6aae`  
		Last Modified: Tue, 02 Jul 2024 01:18:01 GMT  
		Size: 17.2 MB (17151901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baaabb9d206565c384a8980f61cb0b8cd0981e4424a79429b7fc4f0035dd0291`  
		Last Modified: Tue, 02 Jul 2024 01:18:01 GMT  
		Size: 543.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2168fa498f6e7a4f84807a705206a0bd50ee805753e6770fd89e041d8af43a`  
		Last Modified: Tue, 02 Jul 2024 01:18:01 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dac0657b1291ea56f85b8db9a439044dd0a292f53111650bdf0c08ace31d1f0`  
		Last Modified: Tue, 02 Jul 2024 01:18:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6772d9dda27a08b2e303ebe1308388a540802ef5e9e6ade807751524d2a3f7`  
		Last Modified: Tue, 02 Jul 2024 09:52:00 GMT  
		Size: 15.8 MB (15816849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14865a998e91fc65dc30663d446ab2c6a484242d413cc1e54a152dcea0d8274`  
		Last Modified: Tue, 02 Jul 2024 09:51:59 GMT  
		Size: 98.6 KB (98635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b718259c71dd6da33752357960b334a8210509473ae0840f2910d56dad6c155`  
		Last Modified: Tue, 02 Jul 2024 09:51:59 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71228ad5c8bdf178147130725e924400ab6a7fb48a91376a1241bd9ec6061700`  
		Last Modified: Tue, 02 Jul 2024 09:52:01 GMT  
		Size: 52.4 MB (52376003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c3cede826c243d46a571cfb98ec65c9d791cafa97b007b873709152e7ae995`  
		Last Modified: Tue, 02 Jul 2024 09:52:00 GMT  
		Size: 1.5 KB (1509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bca4a4996d1e27e05c6496f801edbbf723b9553fa1cd6d158ae983d8385e12`  
		Last Modified: Tue, 02 Jul 2024 09:52:00 GMT  
		Size: 3.3 KB (3256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b037e880d1c9085999885841dfc3efa3133bcff82cc296fb69c4f9ef0970fee9`  
		Last Modified: Wed, 03 Jul 2024 01:41:14 GMT  
		Size: 1.0 MB (1023114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd15d6ea3ffe2db95e7f6ecaf5ef7b2090ba136213737b9c4b2f18fccc3fb6a9`  
		Last Modified: Wed, 03 Jul 2024 01:41:13 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00e08ade440144dc304e8a270c91090a22a001402badbc83b3c3f298035998b`  
		Last Modified: Wed, 03 Jul 2024 01:41:13 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7215392acbc1da0e4fc5811ebc38f234ef0a1f4831bd66429bbde9ba9acf5a91`  
		Last Modified: Wed, 03 Jul 2024 01:41:15 GMT  
		Size: 22.8 MB (22836952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a34611777988e0ad53e8ef82918c21bbea12db8abf4fe306635c5c9db96bf0`  
		Last Modified: Wed, 03 Jul 2024 01:41:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:27-dind-rootless` - unknown; unknown

```console
$ docker pull docker@sha256:f5acf5ca87e2c7a3332e73b7041c04386ac80f7f77fa2a284dfe6329b1c8a75b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (31012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd08a35ef873f5f46b56f4f832f83913f2019cfa5f31b33533d3701191327f5`

```dockerfile
```

-	Layers:
	-	`sha256:4d1151e0b57213712c976e5083dd75d8baae9b73087a1caa678adbaa2749b124`  
		Last Modified: Wed, 03 Jul 2024 01:41:13 GMT  
		Size: 31.0 KB (31012 bytes)  
		MIME: application/vnd.in-toto+json
