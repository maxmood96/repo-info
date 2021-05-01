## `aerospike:ee-5.3.0.16`

```console
$ docker pull aerospike@sha256:2f77eeeead9bfdf124ffc177aacce958c8bbf83fc2d5c371cbd7f68a3b241ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:ee-5.3.0.16` - linux; amd64

```console
$ docker pull aerospike@sha256:45b3cd4aadabf446ca818939d17d50e31052c591ed47066adcccd273893d4245
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76373431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b10bffc2e710a35ce3fac528357f9bbd3461ab109a07d7f0b7141af1c0b9804b`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Sat, 10 Apr 2021 01:21:54 GMT
ADD file:70cd6967491943999563ddd3ab9abae33791ac320cdc846dc57503cc44f25600 in / 
# Sat, 10 Apr 2021 01:21:54 GMT
CMD ["bash"]
# Thu, 15 Apr 2021 18:19:28 GMT
ENV AEROSPIKE_VERSION=5.3.0.16
# Sat, 01 May 2021 04:47:16 GMT
ENV AEROSPIKE_SHA256=1408e186da1d5bb225a7296091ad32330b6c39c89dc3a45077c7e869c6e80edd
# Sat, 01 May 2021 04:47:36 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libldap-dev libcurl4-openssl-dev   && wget "https://www.aerospike.com/enterprise/download/server/${AEROSPIKE_VERSION}/artifact/debian9" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Sat, 01 May 2021 04:47:37 GMT
COPY file:82161ba7b6e7d24ef9aeee8b19996114e9ff71c3928086ed1e58e01e82ee76a9 in /etc/aerospike/aerospike.template.conf 
# Sat, 01 May 2021 04:47:37 GMT
COPY file:11988df14ff2f0260ab7b8ccb322ee2d343b55791c51356df1d99639d16a6dbc in /entrypoint.sh 
# Sat, 01 May 2021 04:47:37 GMT
EXPOSE 3000 3001 3002
# Sat, 01 May 2021 04:47:37 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Sat, 01 May 2021 04:47:38 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:62deabe7a6db312ed773ccd640cd7cfbf51c22bf466886345684558f1036e358`  
		Last Modified: Sat, 10 Apr 2021 01:28:26 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85cc62177054b327978698863cef2770e45e2fe3006b2f01c4a2da9ddad5e8b6`  
		Last Modified: Sat, 01 May 2021 04:48:25 GMT  
		Size: 53.8 MB (53843051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c33fd0d3c96cdce607f486a81c1d4d966f0134eea9a0097a883ab5cdb933d1`  
		Last Modified: Sat, 01 May 2021 04:48:17 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de1277161537dc75963b96a9bf1009590fb4351ec2d00b54306f72a17f90bc3`  
		Last Modified: Sat, 01 May 2021 04:48:17 GMT  
		Size: 926.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
