## `docker:20-dind-rootless`

```console
$ docker pull docker@sha256:8503c03afa09cadc158a3000c30ae697dc33ddf11eed2d1cabd1d1611f441621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:20-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:bfc2af39af70d97b9e4231204d16445c1a584dd71067128503da5b8e96f42e65
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103136453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82b8ec259815b23643b55c93659d43dfa72f8c1dc26a57489f5348b9d7a9aee1`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:16:58 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Wed, 14 Apr 2021 20:16:59 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:16:59 GMT
ENV DOCKER_VERSION=20.10.6
# Wed, 14 Apr 2021 20:17:06 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-20.10.6.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-20.10.6.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-20.10.6.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-20.10.6.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Wed, 14 Apr 2021 20:17:06 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Wed, 14 Apr 2021 20:17:06 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Wed, 14 Apr 2021 20:17:07 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Wed, 14 Apr 2021 20:17:08 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Wed, 14 Apr 2021 20:17:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 20:17:08 GMT
CMD ["sh"]
# Wed, 14 Apr 2021 20:17:15 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		ip6tables 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Wed, 14 Apr 2021 20:17:16 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 30 Apr 2021 21:19:40 GMT
ENV DIND_COMMIT=42b1175eda071c0e9121e1d64345928384a93df1
# Fri, 30 Apr 2021 21:19:41 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 30 Apr 2021 21:19:42 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Fri, 30 Apr 2021 21:19:42 GMT
VOLUME [/var/lib/docker]
# Fri, 30 Apr 2021 21:19:42 GMT
EXPOSE 2375 2376
# Fri, 30 Apr 2021 21:19:42 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 30 Apr 2021 21:19:42 GMT
CMD []
# Fri, 30 Apr 2021 21:19:47 GMT
RUN apk add --no-cache iproute2
# Fri, 30 Apr 2021 21:19:48 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 30 Apr 2021 21:19:49 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 30 Apr 2021 21:19:51 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-20.10.6.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Fri, 30 Apr 2021 21:19:52 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 30 Apr 2021 21:19:52 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 30 Apr 2021 21:19:53 GMT
USER rootless
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a38b3726f4b24fa93b80450be63ad67fd3239c2f3b83695118d7b1a88447d84`  
		Last Modified: Wed, 14 Apr 2021 20:18:49 GMT  
		Size: 2.1 MB (2050156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5fa5deb334027202841b051d10e7c7137fa3b63e97734309cedf6b48804df5f`  
		Last Modified: Wed, 14 Apr 2021 20:18:45 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7e0e3b754519331113e409b44b7401dda685cba747e0fbb619b907b85e65a6`  
		Last Modified: Wed, 14 Apr 2021 20:18:58 GMT  
		Size: 70.2 MB (70170176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493333e9491fba57ff1ea5b8058546fc5a3e124d325f8720c018568f852e385b`  
		Last Modified: Wed, 14 Apr 2021 20:18:45 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d445cfca767cb2a0dbdc152ed5eeed364db2b6353f8dedf8f917562c116b9b`  
		Last Modified: Wed, 14 Apr 2021 20:18:45 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32eb6dfb922720a338efac9871565ad3ca1a3ac69b540f214e1224bc55191c69`  
		Last Modified: Wed, 14 Apr 2021 20:18:45 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d639a526fd028c25fcf84da7dae5d0ba63ab0a5e132cba88da1ce6f1d40d26d1`  
		Last Modified: Wed, 14 Apr 2021 20:19:17 GMT  
		Size: 6.6 MB (6610563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb69747b337f3c255684e18afcbea89c3e3dc53a0a5b4bd06d4b89db997d2861`  
		Last Modified: Wed, 14 Apr 2021 20:19:15 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e113b274b04ecd11793570ada2f55a1e4c64e0c10db73c1866377cf82cab55`  
		Last Modified: Fri, 30 Apr 2021 21:20:49 GMT  
		Size: 983.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f313182f99204b34385f9d3128987fb558f45fad2f6c789693f11bde444b0fc2`  
		Last Modified: Fri, 30 Apr 2021 21:20:48 GMT  
		Size: 2.5 KB (2512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a00039d212c388ad10e650a9b08e2d08190013c06d352b97bfff521a8dbef8ab`  
		Last Modified: Fri, 30 Apr 2021 21:21:07 GMT  
		Size: 1.1 MB (1131818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6353916d1b7efdd7628289546e1c594b177638abb1de51c73f4faa4cbec1044`  
		Last Modified: Fri, 30 Apr 2021 21:21:08 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba81b9d8073f9d88f889f69edd4821c051bdf3bb8e5b2669bb6a8f2f0b4cb56`  
		Last Modified: Fri, 30 Apr 2021 21:21:07 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7830f18c9fcba58b2a07a3e068f766d1c8c2f224e30aae7a07ec900eebfff539`  
		Last Modified: Fri, 30 Apr 2021 21:21:10 GMT  
		Size: 20.4 MB (20353387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f98f74cdfd2e5cecb631c0b223b2de80cd5eb11fea1a62b98b6b4be77f7d242`  
		Last Modified: Fri, 30 Apr 2021 21:21:07 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
