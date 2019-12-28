## `aerospike:latest`

```console
$ docker pull aerospike@sha256:731cc32514287b64a036949423531019b135024144cc0a20900d89262607ad59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:ed32aa7aeb4cf45ed1c11047137160f36ac45d6c770def344db383a2eee62332
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51855811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ea1131f2079a3c72228544825fa841eaecd9717ffc637b9f2a1428c74c8110`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:06:56 GMT
ENV AEROSPIKE_VERSION=4.8.0.1
# Sat, 28 Dec 2019 05:06:56 GMT
ENV AEROSPIKE_SHA256=143aa9bbecf8d2516d5b69f6e559be926f86c7c2dd7d77723a53ded403acb626
# Sat, 28 Dec 2019 05:07:20 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Sat, 28 Dec 2019 05:07:21 GMT
COPY file:b2afebdf574a22640dc0687630172a267f2dc7857e8cd93254039deab3b62213 in /etc/aerospike/aerospike.template.conf 
# Sat, 28 Dec 2019 05:07:21 GMT
COPY file:688bc1b7dea55c1dc5575a99640936049823d07bac5c920bbace2369fbb27428 in /entrypoint.sh 
# Sat, 28 Dec 2019 05:07:21 GMT
VOLUME [/opt/aerospike/data]
# Sat, 28 Dec 2019 05:07:22 GMT
EXPOSE 3000 3001 3002 3003
# Sat, 28 Dec 2019 05:07:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 28 Dec 2019 05:07:22 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd38fe8509e6a2bb1736b351d0e79476d90fcd469bb3c3e2eb33c9525a39bd7`  
		Last Modified: Sat, 28 Dec 2019 05:07:59 GMT  
		Size: 29.3 MB (29329182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1758ce236298f23bb9f32d1c04b39c8012eec26eea329ffffd3eb52a96455233`  
		Last Modified: Sat, 28 Dec 2019 05:07:48 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ecf27fd22dcc59cced86db8b5feafccae169f36f6c56a50bfc7b87f32cac3d`  
		Last Modified: Sat, 28 Dec 2019 05:07:48 GMT  
		Size: 884.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
