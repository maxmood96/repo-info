## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:62702ba64f0f2ae10243fd84a752c821b161902bbf3256497312568c879e0bdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:latest` - linux; amd64

```console
$ docker pull api-firewall@sha256:1f4f679e3b3e3cec24eeaf6e8bd2d126fdbb9b84c223db0580a2a23cd6c08002
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14196600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ff214038079d3823de64a06957442946da5cab2f304d1bab1f31775e94584b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:58:15 GMT
ENV APIFW_PATH=/opt/api-firewall
# Sat, 16 Mar 2024 07:58:15 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Mar 2024 07:58:15 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Wed, 17 Apr 2024 17:51:19 GMT
ENV APIFIREWALL_VERSION=v0.7.2
# Wed, 17 Apr 2024 17:51:22 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='d37f804498472459ac9e974093d767fb3944c46e6db325a98917b249e063dff0';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='23a202516b26219e250b2adb1e7a905795e91003dadd6209c72ca9c737085481';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='8b3a5b335c4fb6d14ff159875178826dd4e80a10ec3de26ca42ab1ed30123536';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Wed, 17 Apr 2024 17:51:22 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Wed, 17 Apr 2024 17:51:22 GMT
USER api-firewall
# Wed, 17 Apr 2024 17:51:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Apr 2024 17:51:23 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996bf125e6b3d4ba812c8d06e1edb5c9b93b9afcf0b23a4b46709f99f65a1ef0`  
		Last Modified: Sat, 16 Mar 2024 07:58:26 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926f4c1535895073f24a02e9dde0267c269a3119eef996b519eff49e5ef70fd6`  
		Last Modified: Wed, 17 Apr 2024 17:51:39 GMT  
		Size: 10.8 MB (10792496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cce0eb0be60df72eb53ced20cc81b9a24d6feee98389c5058245d819069bcdb`  
		Last Modified: Wed, 17 Apr 2024 17:51:38 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:22de1f839755fa40f007a42f965d39273db51a711ca8a27fad224a7ee8cb3795
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13665829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c512e2823b8b76f170e03bf8953b73bd9300ead03f03e3ae8d413ce7da10d1a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 07 Jun 2024 01:09:46 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 07 Jun 2024 01:09:46 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jun 2024 01:09:47 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Fri, 07 Jun 2024 01:09:47 GMT
ENV APIFIREWALL_VERSION=v0.7.3
# Fri, 07 Jun 2024 01:09:49 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='a381991ff6b0da037a6a1ab0226f2f5cec2d44732fd7c5eb03076da0d46178aa';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='c31ce1b8be28825fd2668206a22970d26d0a7cc958e4ed7aa4cfcbf9865e15e2';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='ac32e358d85015b7aec8ec402d2834927950068b6b2ccbd9279f420c79db2f00';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Fri, 07 Jun 2024 01:09:49 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Fri, 07 Jun 2024 01:09:49 GMT
USER api-firewall
# Fri, 07 Jun 2024 01:09:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 07 Jun 2024 01:09:50 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3473059bcb12b9830e198c36a032b87001c00278292a65f86579bd13a0b0e5bb`  
		Last Modified: Fri, 07 Jun 2024 01:09:58 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a418c736458ed1e0598cb2af4669e72c9d1c584b0acaa50e10403d97ea3703`  
		Last Modified: Fri, 07 Jun 2024 01:09:59 GMT  
		Size: 10.3 MB (10316556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f0f9253e6eb8dd0dd86349bffc25ae92e47d7be143fac96fcfc0c911652d85`  
		Last Modified: Fri, 07 Jun 2024 01:09:58 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; 386

```console
$ docker pull api-firewall@sha256:44034f065c29ccb89c7e4815834bc6a23ffac601bf3c9b12937f28699a8f2932
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12600818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c1d6c3aab6191d22bed77ec8756f60a76a2efa2114e9e33d57c13966d7d661a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 23:52:59 GMT
ENV APIFW_PATH=/opt/api-firewall
# Fri, 15 Mar 2024 23:52:59 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Mar 2024 23:52:59 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Wed, 17 Apr 2024 16:57:32 GMT
ENV APIFIREWALL_VERSION=v0.7.2
# Wed, 17 Apr 2024 16:57:34 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='d37f804498472459ac9e974093d767fb3944c46e6db325a98917b249e063dff0';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='23a202516b26219e250b2adb1e7a905795e91003dadd6209c72ca9c737085481';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='8b3a5b335c4fb6d14ff159875178826dd4e80a10ec3de26ca42ab1ed30123536';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Wed, 17 Apr 2024 16:57:35 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Wed, 17 Apr 2024 16:57:35 GMT
USER api-firewall
# Wed, 17 Apr 2024 16:57:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Apr 2024 16:57:35 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b16feb1c089d261f25d668bc94fb450ae9faaf09472431fb07eaa76ff9fb84`  
		Last Modified: Fri, 15 Mar 2024 23:53:10 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d59d88d4f1f263566209360673e06457c8b2ac183a93217acbfeec21fe3840`  
		Last Modified: Wed, 17 Apr 2024 16:57:53 GMT  
		Size: 9.4 MB (9360193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43679e87d99bf6649bee777299b0405c2fea2af549d7d89ee84d703eedc74944`  
		Last Modified: Wed, 17 Apr 2024 16:57:51 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
