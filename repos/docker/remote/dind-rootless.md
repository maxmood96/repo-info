## `docker:dind-rootless`

```console
$ docker pull docker@sha256:4fc5847227215e29e1c50a846252f7463ae958ed59325becaacd8d65d50509b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `docker:dind-rootless` - linux; amd64

```console
$ docker pull docker@sha256:708826cf96b698b749237d2f2013cf50363d8b54d0a8c8dd89651a336d946499
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97527922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89527d117bacd314548142760ceabb86b486fdc2e48f7267bf0919452775990a`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 04:42:06 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client
# Sat, 18 Jan 2020 04:42:07 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 18 Jan 2020 04:42:07 GMT
ENV DOCKER_CHANNEL=stable
# Fri, 14 Feb 2020 01:19:29 GMT
ENV DOCKER_VERSION=19.03.6
# Fri, 14 Feb 2020 01:19:34 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		dockerd --version; 	docker --version
# Fri, 14 Feb 2020 01:19:34 GMT
COPY file:abb137d24130e7fa2bdd38694af607361ecb688521e60965681e49460964a204 in /usr/local/bin/modprobe 
# Fri, 14 Feb 2020 01:19:34 GMT
COPY file:5b18768029dab8174c9d5957bb39560bde5ef6cba50fbbca222731a0059b449b in /usr/local/bin/ 
# Fri, 14 Feb 2020 01:19:34 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Fri, 14 Feb 2020 01:19:35 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client
# Fri, 14 Feb 2020 01:19:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Feb 2020 01:19:36 GMT
CMD ["sh"]
# Fri, 14 Feb 2020 01:19:42 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		openssl 		shadow-uidmap 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 14 Feb 2020 01:19:43 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 14 Feb 2020 01:19:43 GMT
ENV DIND_COMMIT=37498f009d8bf25fbb6199e8ccd34bed84f2874b
# Fri, 14 Feb 2020 01:19:44 GMT
RUN set -eux; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind
# Fri, 14 Feb 2020 01:19:44 GMT
COPY file:e088145e3deff2cef88e32686489e5e86fdf5669c275cd1a877d11d740ab1a80 in /usr/local/bin/ 
# Fri, 14 Feb 2020 01:19:44 GMT
VOLUME [/var/lib/docker]
# Fri, 14 Feb 2020 01:19:44 GMT
EXPOSE 2375 2376
# Fri, 14 Feb 2020 01:19:44 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 14 Feb 2020 01:19:45 GMT
CMD []
# Fri, 14 Feb 2020 01:19:49 GMT
RUN apk add --no-cache iproute2
# Fri, 14 Feb 2020 01:19:50 GMT
RUN mkdir /run/user && chmod 1777 /run/user
# Fri, 14 Feb 2020 01:19:51 GMT
RUN set -eux; 	adduser -h /home/rootless -g 'Rootless' -D -u 1000 rootless; 	echo 'rootless:100000:65536' >> /etc/subuid; 	echo 'rootless:100000:65536' >> /etc/subgid
# Fri, 14 Feb 2020 01:19:53 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		armv7) dockerArch='armhf' ;; 		aarch64) dockerArch='aarch64' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! wget -O rootless.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-rootless-extras-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-rootless-extras-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file rootless.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		'docker-rootless-extras/vpnkit' 	; 	rm rootless.tgz; 		vpnkit --version
# Fri, 14 Feb 2020 01:19:53 GMT
ENV ROOTLESSKIT_VERSION=0.7.1
# Fri, 14 Feb 2020 01:20:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .rootlesskit-build-deps 		go 		libc-dev 	; 	wget -O rootlesskit.tgz "https://github.com/rootless-containers/rootlesskit/archive/v${ROOTLESSKIT_VERSION}.tar.gz"; 	export GOPATH='/go'; mkdir "$GOPATH"; 	mkdir -p "$GOPATH/src/github.com/rootless-containers/rootlesskit"; 	tar --extract --file rootlesskit.tgz --directory "$GOPATH/src/github.com/rootless-containers/rootlesskit" --strip-components 1; 	rm rootlesskit.tgz; 	go build -o /usr/local/bin/rootlesskit github.com/rootless-containers/rootlesskit/cmd/rootlesskit; 	go build -o /usr/local/bin/rootlesskit-docker-proxy github.com/rootless-containers/rootlesskit/cmd/rootlesskit-docker-proxy; 	rm -rf "$GOPATH"; 	apk del --no-network .rootlesskit-build-deps; 	rootlesskit --version
# Fri, 14 Feb 2020 01:20:06 GMT
RUN set -eux; 	mkdir -p /home/rootless/.local/share/docker; 	chown -R rootless:rootless /home/rootless/.local/share/docker
# Fri, 14 Feb 2020 01:20:06 GMT
VOLUME [/home/rootless/.local/share/docker]
# Fri, 14 Feb 2020 01:20:06 GMT
USER rootless
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd54125436dc48e0d60096d61457bcfd886136eb67815a60210ec67d3793096f`  
		Last Modified: Sat, 18 Jan 2020 04:43:03 GMT  
		Size: 2.4 MB (2425150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d1554c15cbb8c6b81fd21a057c8e97749fb24fd5befeb94ad960d3a350f91f`  
		Last Modified: Sat, 18 Jan 2020 04:43:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a3718af66353ac1b9b61d460169dacea8af2b828fc5a4c145ada71853c1004`  
		Last Modified: Fri, 14 Feb 2020 01:20:39 GMT  
		Size: 64.2 MB (64176130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d685e7204c1caa1e6279ffe73ab17529d60ea1692d2ce9e5bcd82607e72b34`  
		Last Modified: Fri, 14 Feb 2020 01:20:25 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2db148201ed411ce26f0d6f48b5b112ce88292c9ef4bccff01da8443e19e29`  
		Last Modified: Fri, 14 Feb 2020 01:20:25 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419c00a7b0350cd0fdcab8d5856822508e0f6ceefc5220342dabb3aabc23ccaf`  
		Last Modified: Fri, 14 Feb 2020 01:20:25 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cb82cf49416af7d1de7ebe13f3325245f28edd1649b3ae3d845db5b79e1b54`  
		Last Modified: Fri, 14 Feb 2020 01:20:47 GMT  
		Size: 5.6 MB (5587326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db666592efe5d25d406b538d41a46547bc1ee51698fcea3fc61fb9d79ac1b4be`  
		Last Modified: Fri, 14 Feb 2020 01:20:46 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c2ab5c34a68d6bcd5e582c67f7050475fb4964608cfd31f5b7b56889db1019`  
		Last Modified: Fri, 14 Feb 2020 01:20:46 GMT  
		Size: 757.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ab1e2460ab171c3b002e555f427232ba07879374ca4db150cf5a90bbb64c84`  
		Last Modified: Fri, 14 Feb 2020 01:20:46 GMT  
		Size: 2.5 KB (2533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd844ab51ffbfcc6fca8a8ae8a72a52e815636cfd169e728c99c071c7fa48a4b`  
		Last Modified: Fri, 14 Feb 2020 01:20:54 GMT  
		Size: 796.0 KB (796004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5582c4f30ef9cecb7c5f94fe15bd4b99f0f4749367ba458e09f367d873514e2`  
		Last Modified: Fri, 14 Feb 2020 01:20:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00240cac221ddab27d6a4867a0acc924c525ef6b0f9cbb8fec4f899001de28f4`  
		Last Modified: Fri, 14 Feb 2020 01:20:53 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec7222a85ea18e91f7cd193da8846a51e74595113fb1d84c3e68298574f1ff4`  
		Last Modified: Fri, 14 Feb 2020 01:20:56 GMT  
		Size: 9.1 MB (9109454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d05f1f95937d0838abb2c58d1965619d1b96c148c44a6dfdaa5799592826ff0`  
		Last Modified: Fri, 14 Feb 2020 01:20:56 GMT  
		Size: 12.6 MB (12622883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2751b3ef399b03e9983a39a1ee976ac987ff5570c355a1257b39774f6f314226`  
		Last Modified: Fri, 14 Feb 2020 01:20:53 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
