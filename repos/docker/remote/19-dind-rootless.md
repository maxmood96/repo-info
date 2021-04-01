## `docker:19-dind-rootless`

```console
$ docker pull docker@sha256:8023ef461c8b507f4049df73998298289c2ac3d510aca76bac8374a2911f9617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:19-dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:c2fa5d15f05b13d51fcfd194fe336452d156baa2fe74a93d672ab9ee9d4aa198
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94877362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab1ae720603cdb1e92789a7fd95e3bec04c74a2a4835634e512ad63649191bf`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 14:00:03 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Thu, 01 Apr 2021 14:00:04 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 01 Apr 2021 14:00:42 GMT
ENV DOCKER_VERSION=19.03.15
# Thu, 01 Apr 2021 14:00:47 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-19.03.15.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-19.03.15.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-19.03.15.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-19.03.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O docker.tgz "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Thu, 01 Apr 2021 14:00:48 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Thu, 01 Apr 2021 14:00:48 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:48 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 01 Apr 2021 14:00:49 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Thu, 01 Apr 2021 14:00:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:50 GMT
CMD ["sh"]
# Thu, 01 Apr 2021 14:00:55 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Thu, 01 Apr 2021 14:00:56 GMT
RUN set -eux; 	addgroup -S dockremap; 	adduser -S -G dockremap dockremap; 	echo 'dockremap:165536:65536' >> /etc/subuid; 	echo 'dockremap:165536:65536' >> /etc/subgid
# Thu, 01 Apr 2021 14:00:56 GMT
ENV DIND_COMMIT=ed89041433a031cafc0a0f19cfe573c31688d377
# Thu, 01 Apr 2021 14:00:57 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Thu, 01 Apr 2021 14:00:58 GMT
COPY file:ba8ee8770c54e5ecc99314148f702a73a1c00c3ef0cc27ff33581d2dbab7456e in /usr/local/bin/ 
# Thu, 01 Apr 2021 14:00:58 GMT
VOLUME [/var/lib/docker]
# Thu, 01 Apr 2021 14:00:58 GMT
EXPOSE 2375 2376
# Thu, 01 Apr 2021 14:00:58 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Thu, 01 Apr 2021 14:00:58 GMT
CMD []
# Thu, 01 Apr 2021 14:01:03 GMT
RUN apk add --no-cache iproute2
# Thu, 01 Apr 2021 14:01:04 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Thu, 01 Apr 2021 14:01:05 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Thu, 01 Apr 2021 14:01:08 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-rootless-extras-19.03.15.tgz'; 			;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O rootless.tgz "$url"; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/rootlesskit' 		'docker-rootless-extras/rootlesskit-docker-proxy' 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		rootlesskit --version; 	vpnkit --version
# Thu, 01 Apr 2021 14:01:09 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Thu, 01 Apr 2021 14:01:09 GMT
VOLUME [/home/rootless/.local/share/docker]
# Thu, 01 Apr 2021 14:01:09 GMT
USER rootless
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd7def92be556a646233a9d5bc8f76f71c7325a19dca8d162fcbca9ea751236`  
		Last Modified: Thu, 01 Apr 2021 14:01:52 GMT  
		Size: 2.1 MB (2050194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c71d4725b06414fd24a3abd3bee2a59205a840d8b25efc9e7212c24f4dd76`  
		Last Modified: Thu, 01 Apr 2021 14:01:49 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e84bdb1da037f2b156e3a8131fb85cb131e89affba99ae2b7748864ba266dc`  
		Last Modified: Thu, 01 Apr 2021 14:03:39 GMT  
		Size: 62.9 MB (62882941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae5923538977e4280a5ea0bc6901432510d8612c9160d46d9495ed72a92bf97`  
		Last Modified: Thu, 01 Apr 2021 14:03:30 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6751925f010ff3154382d4ee6c31cdef6482519c1b8784380adc3817e992c4c`  
		Last Modified: Thu, 01 Apr 2021 14:03:30 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0097f04ff595a174d3c077e590aeb4eed7ddcf0feb5713ee7f175bfc4a05ab5b`  
		Last Modified: Thu, 01 Apr 2021 14:03:27 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f51334534d69a61dedbfd98d78e9364d5bae13f84562e7d559e842f58269d327`  
		Last Modified: Thu, 01 Apr 2021 14:03:55 GMT  
		Size: 6.6 MB (6569706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d301369a212ffb435db229cf332268ca39abcf482eeed3c5deaa03304fd321`  
		Last Modified: Thu, 01 Apr 2021 14:03:54 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80a6f4322ad475e8b9fba6fb462d8ff80ebb28596e6d973fc18e8d748754164`  
		Last Modified: Thu, 01 Apr 2021 14:03:53 GMT  
		Size: 932.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97439c400a1f9427e2a2e8e0581504f4e64ac21311a83f6ebdbafc91bd15eb5c`  
		Last Modified: Thu, 01 Apr 2021 14:03:53 GMT  
		Size: 2.5 KB (2507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e73dbffe5a55fe14967bdd47a418c821712f5952da8f4d45f10450c5ce6f3f`  
		Last Modified: Thu, 01 Apr 2021 14:04:12 GMT  
		Size: 1.1 MB (1131563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2c536df88aa50d092aa553e47f1e6daa72adf9d20105d6c61283253c7ae118`  
		Last Modified: Thu, 01 Apr 2021 14:04:11 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b5ea595ed45305d464afbc3aa04fc621eb6dbf3ae0aa6057091d6472fffd97`  
		Last Modified: Thu, 01 Apr 2021 14:04:11 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e337b6f794aa5bf5b618857d55b2314dde080241106ecced70fa0cb285334a`  
		Last Modified: Thu, 01 Apr 2021 14:04:15 GMT  
		Size: 19.4 MB (19422690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0dad659d908561f0ad90d499aa0957876110fe95caca7a46e44905b3316ba3`  
		Last Modified: Thu, 01 Apr 2021 14:04:11 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
