## `aerospike:latest`

```console
$ docker pull aerospike@sha256:8f7c5a533c457b7a7a4e99341674ca0e8ee17ff74e1122f2d6532d06fec49c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:9712a70abbc455a29035aff519bfcff2fd13f2395e05661611b9e1eb4ca228d4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74775088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5377e1918cb0ef0e71ba78d7e6e8d115da34c94e8dec79d193f82e18ab34fc51`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Sat, 10 Apr 2021 01:21:54 GMT
ADD file:70cd6967491943999563ddd3ab9abae33791ac320cdc846dc57503cc44f25600 in / 
# Sat, 10 Apr 2021 01:21:54 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 06:10:04 GMT
ENV AEROSPIKE_VERSION=5.5.0.7
# Sat, 10 Apr 2021 06:10:04 GMT
ENV AEROSPIKE_SHA256=43cc7c0b135fa8a0186a8ce9b5f923660e59e3ef8ec32a742a5b533c1d3caaa3
# Sat, 10 Apr 2021 06:10:29 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Sat, 10 Apr 2021 06:10:29 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Sat, 10 Apr 2021 06:10:30 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Sat, 10 Apr 2021 06:10:30 GMT
EXPOSE 3000 3001 3002 3003
# Sat, 10 Apr 2021 06:10:30 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Sat, 10 Apr 2021 06:10:30 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:62deabe7a6db312ed773ccd640cd7cfbf51c22bf466886345684558f1036e358`  
		Last Modified: Sat, 10 Apr 2021 01:28:26 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad8b703df239d9ef1039174116954bc74604106d065f0f0e3773f027ac7f6dd`  
		Last Modified: Sat, 10 Apr 2021 06:11:35 GMT  
		Size: 52.2 MB (52244768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20772210df85e3911e56d8d8794582c95c062e1782010df96b349cfc1683a516`  
		Last Modified: Sat, 10 Apr 2021 06:11:25 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db8ab26f8f395bf6a55411a5485990b23068c5d9b7463f8449e3c31b3e06571`  
		Last Modified: Sat, 10 Apr 2021 06:11:25 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
