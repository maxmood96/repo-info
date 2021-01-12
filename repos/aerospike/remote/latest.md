## `aerospike:latest`

```console
$ docker pull aerospike@sha256:bb37c0dadc90754744c3c22cd6397fd9afd920fce320b8cd3e62769dd486733e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:3b8a13201f6efe83d2fc01806cc5c5c21d5c177df007a65ee08a5c25899ee219
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74707418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db413a561186e4bfeb27f54039fecbff828ca5c1a5982f5342f1cd10a9014d52`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:58 GMT
ADD file:f03e68a10b84e2342cfffbb8cdec1117c7f5e5d0dd004072e84efb62cfdf157c in / 
# Fri, 11 Dec 2020 02:08:58 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:21:31 GMT
ENV AEROSPIKE_VERSION=5.3.0.6
# Tue, 12 Jan 2021 00:21:31 GMT
ENV AEROSPIKE_SHA256=f8d19a6274923c3585810cdbdcac0aa3c3aaa507f032c6733c0168692bb188c5
# Tue, 12 Jan 2021 00:21:54 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Tue, 12 Jan 2021 00:21:54 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Tue, 12 Jan 2021 00:21:54 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Tue, 12 Jan 2021 00:21:54 GMT
EXPOSE 3000 3001 3002 3003
# Tue, 12 Jan 2021 00:21:55 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Tue, 12 Jan 2021 00:21:55 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:e50c3c9ef5a201a24959788dcbc7ebf88d95c63e132a4d7396ce541127afd88e`  
		Last Modified: Fri, 11 Dec 2020 02:15:43 GMT  
		Size: 22.5 MB (22527860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88a7a594e66f9bebdf8a26517efb1c122452ca2f31b8902b38ac3ab16f6950c`  
		Last Modified: Tue, 12 Jan 2021 00:22:46 GMT  
		Size: 52.2 MB (52177504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:965975e1febd6ec81b32165c9475c12d4d9cae8bd8364bdb950bd63236510628`  
		Last Modified: Tue, 12 Jan 2021 00:22:36 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574e5a66699492afe0747311a4d25dca3658dbdd45a3e72fe194adbf2c64f597`  
		Last Modified: Tue, 12 Jan 2021 00:22:36 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
