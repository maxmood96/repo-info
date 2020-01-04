<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:4.6.0.10`](#aerospike46010)
-	[`aerospike:4.7.0.7`](#aerospike4707)
-	[`aerospike:4.8.0.2`](#aerospike4802)
-	[`aerospike:latest`](#aerospikelatest)

## `aerospike:4.6.0.10`

```console
$ docker pull aerospike@sha256:18e9c7053671dedd3bf2ab7964c2d9de40e9b0d12ac8cfd29708a0702178fbd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:4.6.0.10` - linux; amd64

```console
$ docker pull aerospike@sha256:49c27ac778220d70a473db156aaa5bfb063cc7ceb553695961655714af93633c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51656516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c5d7a9c7a191a6b86cff94be4ea5cf5196c9b6e8ac49c79a8fd3b97e7284ab0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 04 Jan 2020 05:20:24 GMT
ENV AEROSPIKE_VERSION=4.6.0.10
# Sat, 04 Jan 2020 05:20:24 GMT
ENV AEROSPIKE_SHA256=502df2500bfeeafbf4d9859170a359a403cd65dde4728e1566397a7d5f5ea8b7
# Sat, 04 Jan 2020 05:20:41 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Sat, 04 Jan 2020 05:20:41 GMT
COPY file:b2afebdf574a22640dc0687630172a267f2dc7857e8cd93254039deab3b62213 in /etc/aerospike/aerospike.template.conf 
# Sat, 04 Jan 2020 05:20:42 GMT
COPY file:688bc1b7dea55c1dc5575a99640936049823d07bac5c920bbace2369fbb27428 in /entrypoint.sh 
# Sat, 04 Jan 2020 05:20:42 GMT
VOLUME [/opt/aerospike/data]
# Sat, 04 Jan 2020 05:20:42 GMT
EXPOSE 3000 3001 3002 3003
# Sat, 04 Jan 2020 05:20:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 04 Jan 2020 05:20:42 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cf7c885a90192bb79cd5f23b3fd8079aef526cae89daef93caf6ecb6f291a5`  
		Last Modified: Sat, 04 Jan 2020 05:21:44 GMT  
		Size: 29.1 MB (29129891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf0c5e40344bd52cd31b556ee731036b406a36759a6e30c61d0828da8a0fd30`  
		Last Modified: Sat, 04 Jan 2020 05:21:39 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6424ce4ffac719b3e3fd14dbd016e89a80f9db71e363fdc7da937c748468ee99`  
		Last Modified: Sat, 04 Jan 2020 05:21:39 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:4.7.0.7`

```console
$ docker pull aerospike@sha256:991f304f859c116fe37e99bcaaec00a64920c05ad8fc26472a127260a37f21ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:4.7.0.7` - linux; amd64

```console
$ docker pull aerospike@sha256:4836d2abe649059a88be7ae6d1c274a0502d285d880023fa69fd2275f7ff3914
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51778376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60214266dc15a990f5dc33a31afff651dfb71bad74d2c98b6ed137fddf0f4d1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 04 Jan 2020 05:20:48 GMT
ENV AEROSPIKE_VERSION=4.7.0.7
# Sat, 04 Jan 2020 05:20:48 GMT
ENV AEROSPIKE_SHA256=8293f296415109d0ac98147bab1687b6b0bdfcf6530432439c65866e9d4183bf
# Sat, 04 Jan 2020 05:21:04 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Sat, 04 Jan 2020 05:21:05 GMT
COPY file:b2afebdf574a22640dc0687630172a267f2dc7857e8cd93254039deab3b62213 in /etc/aerospike/aerospike.template.conf 
# Sat, 04 Jan 2020 05:21:05 GMT
COPY file:688bc1b7dea55c1dc5575a99640936049823d07bac5c920bbace2369fbb27428 in /entrypoint.sh 
# Sat, 04 Jan 2020 05:21:05 GMT
VOLUME [/opt/aerospike/data]
# Sat, 04 Jan 2020 05:21:05 GMT
EXPOSE 3000 3001 3002 3003
# Sat, 04 Jan 2020 05:21:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 04 Jan 2020 05:21:06 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f79cdb403a5c20332282e31c1755f2ab17cd59c39feb73f57322d0ebc9da982`  
		Last Modified: Sat, 04 Jan 2020 05:21:59 GMT  
		Size: 29.3 MB (29251748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e621dcc8c2a5c5ea9fa46642ae4f1c7d4a75a4220c0822422c9798904a7882a`  
		Last Modified: Sat, 04 Jan 2020 05:21:48 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ed02087c165b352bb3351139555cc8909bce7a1787c4fde341177de9db74d5`  
		Last Modified: Sat, 04 Jan 2020 05:21:47 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:4.8.0.2`

```console
$ docker pull aerospike@sha256:583278e8f9512beb132abf9a96cd1986696b26a70ac4d47d0e3455fd1b87caa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:4.8.0.2` - linux; amd64

```console
$ docker pull aerospike@sha256:00af80d2f9d29ca7b51c81e807c3b54ac3052aa0fbba912d33bb7b80354a72ab
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51855677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b877b7c08dc6e9e33ebed4e6de08aa12c098ec8d532e957e2207f5fdfd94a26d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 04 Jan 2020 05:21:12 GMT
ENV AEROSPIKE_VERSION=4.8.0.2
# Sat, 04 Jan 2020 05:21:13 GMT
ENV AEROSPIKE_SHA256=73b90cbf5cbd7874033efdb8cd4d31376702ea9766b96dc7627701bea726c889
# Sat, 04 Jan 2020 05:21:29 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Sat, 04 Jan 2020 05:21:29 GMT
COPY file:b2afebdf574a22640dc0687630172a267f2dc7857e8cd93254039deab3b62213 in /etc/aerospike/aerospike.template.conf 
# Sat, 04 Jan 2020 05:21:29 GMT
COPY file:688bc1b7dea55c1dc5575a99640936049823d07bac5c920bbace2369fbb27428 in /entrypoint.sh 
# Sat, 04 Jan 2020 05:21:30 GMT
VOLUME [/opt/aerospike/data]
# Sat, 04 Jan 2020 05:21:30 GMT
EXPOSE 3000 3001 3002 3003
# Sat, 04 Jan 2020 05:21:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 04 Jan 2020 05:21:30 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269631b6ed7d942038ff564bdb5c65603a40cd56f83031c5603c2a4d7745be33`  
		Last Modified: Sat, 04 Jan 2020 05:22:08 GMT  
		Size: 29.3 MB (29329053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52b89a013931352a8a3abe2893ad0fc188fb1b336b402afa85d53eacaf54d1d`  
		Last Modified: Sat, 04 Jan 2020 05:22:03 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2d644b7778f4ddd52fddcaad1c0f35301c5f14c344e5f43bb48373e8203a59`  
		Last Modified: Sat, 04 Jan 2020 05:22:03 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:latest`

```console
$ docker pull aerospike@sha256:583278e8f9512beb132abf9a96cd1986696b26a70ac4d47d0e3455fd1b87caa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:00af80d2f9d29ca7b51c81e807c3b54ac3052aa0fbba912d33bb7b80354a72ab
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51855677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b877b7c08dc6e9e33ebed4e6de08aa12c098ec8d532e957e2207f5fdfd94a26d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 04 Jan 2020 05:21:12 GMT
ENV AEROSPIKE_VERSION=4.8.0.2
# Sat, 04 Jan 2020 05:21:13 GMT
ENV AEROSPIKE_SHA256=73b90cbf5cbd7874033efdb8cd4d31376702ea9766b96dc7627701bea726c889
# Sat, 04 Jan 2020 05:21:29 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Sat, 04 Jan 2020 05:21:29 GMT
COPY file:b2afebdf574a22640dc0687630172a267f2dc7857e8cd93254039deab3b62213 in /etc/aerospike/aerospike.template.conf 
# Sat, 04 Jan 2020 05:21:29 GMT
COPY file:688bc1b7dea55c1dc5575a99640936049823d07bac5c920bbace2369fbb27428 in /entrypoint.sh 
# Sat, 04 Jan 2020 05:21:30 GMT
VOLUME [/opt/aerospike/data]
# Sat, 04 Jan 2020 05:21:30 GMT
EXPOSE 3000 3001 3002 3003
# Sat, 04 Jan 2020 05:21:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 04 Jan 2020 05:21:30 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269631b6ed7d942038ff564bdb5c65603a40cd56f83031c5603c2a4d7745be33`  
		Last Modified: Sat, 04 Jan 2020 05:22:08 GMT  
		Size: 29.3 MB (29329053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52b89a013931352a8a3abe2893ad0fc188fb1b336b402afa85d53eacaf54d1d`  
		Last Modified: Sat, 04 Jan 2020 05:22:03 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2d644b7778f4ddd52fddcaad1c0f35301c5f14c344e5f43bb48373e8203a59`  
		Last Modified: Sat, 04 Jan 2020 05:22:03 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
