<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:4.7.0.13`](#aerospike47013)
-	[`aerospike:4.8.0.9`](#aerospike4809)
-	[`aerospike:4.9.0.5`](#aerospike4905)
-	[`aerospike:latest`](#aerospikelatest)

## `aerospike:4.7.0.13`

```console
$ docker pull aerospike@sha256:51a54080afce3ccae698b25d6988ff18ed5cceeeba4f5dc21b510ebbbe4c6399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:4.7.0.13` - linux; amd64

```console
$ docker pull aerospike@sha256:5a034dbe5278996e9f530563a644596b4e3cd86d062a0700199de452aa2b2338
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51769409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d9ff072fc5fc2b7e1ef31f7568cb54f8d472d3cc453e488b77408242e068a8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Mon, 20 Apr 2020 23:19:28 GMT
ENV AEROSPIKE_VERSION=4.7.0.13
# Mon, 20 Apr 2020 23:19:29 GMT
ENV AEROSPIKE_SHA256=05585d9f2e9e2e066d6fc2845bd83f764b104e84140b614b53fb71309e47695a
# Mon, 20 Apr 2020 23:19:45 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Mon, 20 Apr 2020 23:19:46 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Mon, 20 Apr 2020 23:19:46 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Mon, 20 Apr 2020 23:19:46 GMT
VOLUME [/opt/aerospike/data]
# Mon, 20 Apr 2020 23:19:46 GMT
EXPOSE 3000 3001 3002 3003
# Mon, 20 Apr 2020 23:19:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Apr 2020 23:19:47 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69371f60ded8698078f450b4a1a79dc0a58d3eebe677801cf4b9663ceb93843`  
		Last Modified: Mon, 20 Apr 2020 23:20:27 GMT  
		Size: 29.3 MB (29253882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b5b7bb6aac5fb1c2d485294d05233dc0b350fa2da59a4c4f89ae09fb245885`  
		Last Modified: Mon, 20 Apr 2020 23:20:22 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e27d24a094d447dc3b8c864efa33743d5581c980e7b515be0ad287548f9f243`  
		Last Modified: Mon, 20 Apr 2020 23:20:23 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:4.8.0.9`

```console
$ docker pull aerospike@sha256:304fbdd9a21a1337b6819211151bf8414da358ddae11dcb9e83467c11a4cd204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:4.8.0.9` - linux; amd64

```console
$ docker pull aerospike@sha256:38784523a0b8284db783c5a4a0f62c3fd4bba886120b97c1ddeea5af372a1c0d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51846297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaca8f068711ebcc8978290caba2fe283e0018916ea48f63f9bf471ba0a563d8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Mon, 20 Apr 2020 23:19:53 GMT
ENV AEROSPIKE_VERSION=4.8.0.9
# Mon, 20 Apr 2020 23:19:54 GMT
ENV AEROSPIKE_SHA256=3af1b8c97d73d05054582c8941d435bea55b7ead9b04d2df42f1e9990ab7e0c3
# Mon, 20 Apr 2020 23:20:10 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Mon, 20 Apr 2020 23:20:11 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Mon, 20 Apr 2020 23:20:11 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Mon, 20 Apr 2020 23:20:11 GMT
VOLUME [/opt/aerospike/data]
# Mon, 20 Apr 2020 23:20:11 GMT
EXPOSE 3000 3001 3002 3003
# Mon, 20 Apr 2020 23:20:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Apr 2020 23:20:12 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2cc211c05a100157850c9ec7a888fcad4a54511a7dcbbc94e4473128b7ab5d5`  
		Last Modified: Mon, 20 Apr 2020 23:20:35 GMT  
		Size: 29.3 MB (29330770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e83e45229152f42ff1cc23afa8f06990f586960bf93133675cfa4b5ec28ffa0`  
		Last Modified: Mon, 20 Apr 2020 23:20:30 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d789f2efa3ec78c2168a07bfd7f5a195cd008eb39fdb7e500b6709b2368899`  
		Last Modified: Mon, 20 Apr 2020 23:20:31 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:4.9.0.5`

```console
$ docker pull aerospike@sha256:46dae4b19bd6bba3e27ba6642e858f42e54472131679af23967c6b05e1ef3687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:4.9.0.5` - linux; amd64

```console
$ docker pull aerospike@sha256:82066b1f48e983815a1e5548cbd447f4b8615e427239ef0a46455656809b960d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53186034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af52663174798c74c6601751b108b0a89ed27e16ba5ccf57fd7519acd1b51fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Wed, 22 Apr 2020 23:19:31 GMT
ENV AEROSPIKE_VERSION=4.9.0.5
# Wed, 22 Apr 2020 23:19:31 GMT
ENV AEROSPIKE_SHA256=7e9b345020e987d1a4d1c91034a8054c97fd80a0c917a8da04d4aad9127e8fe2
# Wed, 22 Apr 2020 23:19:48 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Wed, 22 Apr 2020 23:19:49 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Wed, 22 Apr 2020 23:19:49 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Wed, 22 Apr 2020 23:19:49 GMT
VOLUME [/opt/aerospike/data]
# Wed, 22 Apr 2020 23:19:49 GMT
EXPOSE 3000 3001 3002 3003
# Wed, 22 Apr 2020 23:19:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2020 23:19:50 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da346537327e3ee7e05d5aa70da7b6864b9ed98fde21850f34a7ef6bf655655`  
		Last Modified: Wed, 22 Apr 2020 23:20:04 GMT  
		Size: 30.7 MB (30670508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba1e580609deca966900760a2d9e1f0a0e9ce21cac4cf31788475fd8bd8845f`  
		Last Modified: Wed, 22 Apr 2020 23:19:59 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaace1508aa683604b4a01094c1cd1b6c94fb15022c71d9ec61f0125c1bea00f`  
		Last Modified: Wed, 22 Apr 2020 23:20:00 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:latest`

```console
$ docker pull aerospike@sha256:46dae4b19bd6bba3e27ba6642e858f42e54472131679af23967c6b05e1ef3687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:82066b1f48e983815a1e5548cbd447f4b8615e427239ef0a46455656809b960d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53186034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af52663174798c74c6601751b108b0a89ed27e16ba5ccf57fd7519acd1b51fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Wed, 22 Apr 2020 23:19:31 GMT
ENV AEROSPIKE_VERSION=4.9.0.5
# Wed, 22 Apr 2020 23:19:31 GMT
ENV AEROSPIKE_SHA256=7e9b345020e987d1a4d1c91034a8054c97fd80a0c917a8da04d4aad9127e8fe2
# Wed, 22 Apr 2020 23:19:48 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Wed, 22 Apr 2020 23:19:49 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Wed, 22 Apr 2020 23:19:49 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Wed, 22 Apr 2020 23:19:49 GMT
VOLUME [/opt/aerospike/data]
# Wed, 22 Apr 2020 23:19:49 GMT
EXPOSE 3000 3001 3002 3003
# Wed, 22 Apr 2020 23:19:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2020 23:19:50 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da346537327e3ee7e05d5aa70da7b6864b9ed98fde21850f34a7ef6bf655655`  
		Last Modified: Wed, 22 Apr 2020 23:20:04 GMT  
		Size: 30.7 MB (30670508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba1e580609deca966900760a2d9e1f0a0e9ce21cac4cf31788475fd8bd8845f`  
		Last Modified: Wed, 22 Apr 2020 23:19:59 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaace1508aa683604b4a01094c1cd1b6c94fb15022c71d9ec61f0125c1bea00f`  
		Last Modified: Wed, 22 Apr 2020 23:20:00 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
