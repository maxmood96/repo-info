## `docker:20-dind-rootless`

```console
$ docker pull docker@sha256:4f6f77d22464c33e82b69dae2335e85b1c0b9c463dac8035465b9778a5d3221e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `docker:20-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:d1a3e15aeecebf41c8d9b00747ed033cd946c48645af94d9ee4e1c80ade2bb6f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 MB (96432886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deda3d6ded5613af44013e788c53e5a0d7e86079e756c6b9014b1b4e7f8a73a9`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:02:42 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 11:02:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 11:02:43 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 05 Apr 2022 11:02:49 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Apr 2022 11:02:49 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Apr 2022 11:02:49 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Apr 2022 11:02:49 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Apr 2022 11:02:50 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Apr 2022 11:02:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 11:02:50 GMT
CMD ["sh"]
# Tue, 05 Apr 2022 11:02:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 05 Apr 2022 11:02:56 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 05 Apr 2022 11:02:56 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 05 Apr 2022 11:02:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 05 Apr 2022 11:02:57 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 05 Apr 2022 11:02:57 GMT
VOLUME [/var/lib/docker]
# Tue, 05 Apr 2022 11:02:57 GMT
EXPOSE 2375 2376
# Tue, 05 Apr 2022 11:02:57 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 05 Apr 2022 11:02:57 GMT
CMD []
# Tue, 05 Apr 2022 11:03:01 GMT
RUN apk add --no-cache iproute2
# Tue, 05 Apr 2022 11:03:02 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Tue, 05 Apr 2022 11:03:02 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Tue, 05 Apr 2022 11:03:18 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Tue, 05 Apr 2022 11:03:18 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Tue, 05 Apr 2022 11:03:19 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 05 Apr 2022 11:03:19 GMT
USER rootless
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60e3bd692ff4ff4d32e553972ecdb6781dd2c64e1b8ce0ea011f36caf237816`  
		Last Modified: Tue, 05 Apr 2022 11:03:50 GMT  
		Size: 2.0 MB (1969568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36df9e333c707e825d69eb4d7bff03bb32304316c692a4a4a6cdf2860b94ccd9`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:335507422d7f6524df2b4fc0f8a0c78b1c1e61e8d308dafd67da8da9c39f55d6`  
		Last Modified: Tue, 05 Apr 2022 11:03:58 GMT  
		Size: 64.6 MB (64611599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b18125cc2d27af3a9197591ac217431c4fc6064285b86e53999fad8e17c6cee`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf930f6823a9774d33765edbd3dcc9ea0ea8e5463ce7dade2e323da18e2bbc98`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7048a2a9629e4e35e89c70f592f04400913adf651643325e83f31e7618599d58`  
		Last Modified: Tue, 05 Apr 2022 11:03:47 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0af8a24b3d99f5d1b97b69005e6e5e973fd76878eb63382937c166cdf5441e`  
		Last Modified: Tue, 05 Apr 2022 11:04:16 GMT  
		Size: 6.7 MB (6734743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c69def9f2284d6ca51f913d19f45240f7051c275501a791efcbf2390a18704`  
		Last Modified: Tue, 05 Apr 2022 11:04:15 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2998284497aa95875ef53929de1b46642eec185be6f5dd1a1e772dbce1761102`  
		Last Modified: Tue, 05 Apr 2022 11:04:15 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67900e1c727f6291a49060673983d9297ce9a47b8e599f10fb276e8ff7973f4f`  
		Last Modified: Tue, 05 Apr 2022 11:04:15 GMT  
		Size: 2.7 KB (2748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b588ce9e8fbc77fa67055ed6052e4298508b1fb1b243a0c235fe33418ebaf1c5`  
		Last Modified: Tue, 05 Apr 2022 11:04:43 GMT  
		Size: 1.2 MB (1161981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1b74acd02dbc4e96821b38c1e1c58a37727ed03f82437cab1656c15e1d5b16`  
		Last Modified: Tue, 05 Apr 2022 11:04:43 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b219f357717a1ca5ecae5a8f6141cb714f5782dc31f2ceaa63c7da45c89a42`  
		Last Modified: Tue, 05 Apr 2022 11:04:43 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e307cac3961eec1242ccb911c3fb275f1287855f424c45c1d79e7edb756a4b89`  
		Last Modified: Tue, 05 Apr 2022 11:04:46 GMT  
		Size: 19.1 MB (19131830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11dca8585ce11aea5a2421a5b4d5d811c7ac4669e739d034620f7f2a7ef23c3`  
		Last Modified: Tue, 05 Apr 2022 11:04:43 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:20-dind-rootless` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:102c22b1ecbff700312a32c774ff3ffd2c46f10cc9c6ccc0f86af75cb8176daa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92134365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0129c6606ce03bd35648628f0576fc846da21239569efa33423ba550f6b1ce54`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 08:57:00 GMT
RUN apk add --no-cache 		ca-certificates 		libc6-compat 		openssh-client
# Tue, 05 Apr 2022 08:57:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 08:57:01 GMT
ENV DOCKER_VERSION=20.10.14
# Tue, 05 Apr 2022 08:57:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.14.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.14.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Tue, 05 Apr 2022 08:57:07 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Tue, 05 Apr 2022 08:57:08 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Tue, 05 Apr 2022 08:57:08 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Tue, 05 Apr 2022 08:57:09 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Tue, 05 Apr 2022 08:57:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Apr 2022 08:57:11 GMT
CMD ["sh"]
# Tue, 05 Apr 2022 08:57:21 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 05 Apr 2022 08:57:22 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 05 Apr 2022 08:57:23 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Tue, 05 Apr 2022 08:57:24 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Tue, 05 Apr 2022 08:57:26 GMT
COPY file:45c7926c5d79023b457ad24274c893b1fc21f241bed46421dc901b8237045f17 in /usr/local/bin/ 
# Tue, 05 Apr 2022 08:57:26 GMT
VOLUME [/var/lib/docker]
# Tue, 05 Apr 2022 08:57:27 GMT
EXPOSE 2375 2376
# Tue, 05 Apr 2022 08:57:28 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 05 Apr 2022 08:57:29 GMT
CMD []
# Tue, 05 Apr 2022 08:57:37 GMT
RUN apk add --no-cache iproute2
# Tue, 05 Apr 2022 08:57:37 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Tue, 05 Apr 2022 08:57:38 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Tue, 05 Apr 2022 08:57:40 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.14.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-rootless-extras-20.10.14.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Tue, 05 Apr 2022 08:57:41 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Tue, 05 Apr 2022 08:57:42 GMT
VOLUME [/home/rootless/.local/share/docker]
# Tue, 05 Apr 2022 08:57:43 GMT
USER rootless
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b8a1a2bc336776643f1641eb7c6c2c8fbe180e51541b40d7abec0ceb17668b`  
		Last Modified: Tue, 05 Apr 2022 08:58:34 GMT  
		Size: 1.9 MB (1938913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa25d67de920b612e26aef152b86d46e8cd4eb0e7e991d33f616108107c752e3`  
		Last Modified: Tue, 05 Apr 2022 08:58:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03acc3d19634c8933a32eec790bea497e6cb2aa8f1d3d907767a8b04822c7385`  
		Last Modified: Tue, 05 Apr 2022 08:58:40 GMT  
		Size: 58.6 MB (58565759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0111c96643ec7aae5a4c706e059b855a3c4e91100c63903c4008dc6f1f91cb86`  
		Last Modified: Tue, 05 Apr 2022 08:58:31 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62420f2b46a4ea3baef867a8fc35c1edbe11d37e4d41cd7edee7216483cf69b`  
		Last Modified: Tue, 05 Apr 2022 08:58:31 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46884770b98e15a8879e0af3cd85abcc6c6ff1cec480fc0d1c35bc7d38a11f7`  
		Last Modified: Tue, 05 Apr 2022 08:58:31 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f4ad117037b81b9224d076dd4aefc95febb995806d9eb392aa71d24d1e6d17`  
		Last Modified: Tue, 05 Apr 2022 08:59:01 GMT  
		Size: 6.6 MB (6615590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc1b7685ea6803933ff929fc8f998e000d55c97e0dee19cb86f659fa95b6e1fa`  
		Last Modified: Tue, 05 Apr 2022 08:59:01 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1aa23baa90e93fa870d6defcc88be8db2d3566df1e9c17bf1dd2c4d446a778`  
		Last Modified: Tue, 05 Apr 2022 08:59:00 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8389b10af9ec7d0c040b6d923a61d552aa26ff55531dbe438d8d78dedf9ca2ed`  
		Last Modified: Tue, 05 Apr 2022 08:59:00 GMT  
		Size: 2.7 KB (2744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2538ca5f802703a6aa56d844c38db1458fe6edb7b7c94364fe886657a82184d7`  
		Last Modified: Tue, 05 Apr 2022 08:59:23 GMT  
		Size: 1.2 MB (1177951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef858bd48ea44d965c27c2e18c949ccbfb3b69907b09545efae43761739b26b`  
		Last Modified: Tue, 05 Apr 2022 08:59:23 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fccb2cbf02520d2d7215537dfdacff625816e1e81acaf5f2063271abd2ad6548`  
		Last Modified: Tue, 05 Apr 2022 08:59:22 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d16c036cdaac00e98747ce1420e3f555d85851b8ca5a40aa30b623d564259a`  
		Last Modified: Tue, 05 Apr 2022 08:59:26 GMT  
		Size: 21.1 MB (21111236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c040bfe441d48e06157646370311a0970df44d565593a546413e33cd44fa7dd6`  
		Last Modified: Tue, 05 Apr 2022 08:59:22 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
