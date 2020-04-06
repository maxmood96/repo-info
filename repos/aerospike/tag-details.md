<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:4.6.0.14`](#aerospike46014)
-	[`aerospike:4.7.0.12`](#aerospike47012)
-	[`aerospike:4.8.0.8`](#aerospike4808)
-	[`aerospike:latest`](#aerospikelatest)

## `aerospike:4.6.0.14`

```console
$ docker pull aerospike@sha256:ec871fc964f8c41c36d8917f41479912428721c58f46e7416643966d38aed2c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:4.6.0.14` - linux; amd64

```console
$ docker pull aerospike@sha256:2d02bde59921e707365cd76d38c5ca519ed38bea6765c989ea9dab3a52b55453
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51647399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ebd4226b7388923d77439b6d09c9fb011747d18713ca99ea79d197b7b6e9fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:08 GMT
ADD file:e077f4d014ea0869fc4b3d5a3e6b3c8b792a97a8b4a328f33a994369225ff222 in / 
# Tue, 31 Mar 2020 01:24:08 GMT
CMD ["bash"]
# Mon, 06 Apr 2020 20:19:21 GMT
ENV AEROSPIKE_VERSION=4.6.0.14
# Mon, 06 Apr 2020 20:19:21 GMT
ENV AEROSPIKE_SHA256=bd0596f74de3f529a689764cc0061e97cd06a646d0ca7ae72974ee77f62cdb42
# Mon, 06 Apr 2020 20:19:46 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Mon, 06 Apr 2020 20:19:46 GMT
COPY file:b2afebdf574a22640dc0687630172a267f2dc7857e8cd93254039deab3b62213 in /etc/aerospike/aerospike.template.conf 
# Mon, 06 Apr 2020 20:19:46 GMT
COPY file:688bc1b7dea55c1dc5575a99640936049823d07bac5c920bbace2369fbb27428 in /entrypoint.sh 
# Mon, 06 Apr 2020 20:19:46 GMT
VOLUME [/opt/aerospike/data]
# Mon, 06 Apr 2020 20:19:47 GMT
EXPOSE 3000 3001 3002 3003
# Mon, 06 Apr 2020 20:19:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Apr 2020 20:19:47 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:48839397421a64189661c2b86a34eb515d09a28204587a2b06b59df9f6e2d786`  
		Last Modified: Tue, 31 Mar 2020 01:29:28 GMT  
		Size: 22.5 MB (22513374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:089bb51d16a60be24011e5bdbd01e49b2c2c604430821f6d167115924401e904`  
		Last Modified: Mon, 06 Apr 2020 20:20:50 GMT  
		Size: 29.1 MB (29132009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d0933e0a358a5dee6c234a6a129482e32bdae0e40026186d791e553f868bea`  
		Last Modified: Mon, 06 Apr 2020 20:20:44 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b7712013ea859c9ea80be1613742ab9d70033b3638f14441d08402a35f7ce4`  
		Last Modified: Mon, 06 Apr 2020 20:20:44 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:4.7.0.12`

```console
$ docker pull aerospike@sha256:ba2381650fecd678192971f8e3e2cd7a0da6e2d22f5e1ceef4d28ba62ff1d893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:4.7.0.12` - linux; amd64

```console
$ docker pull aerospike@sha256:2b52d5b194024ef296c5acd0040452c58e6ee8f7bd8a1de00181a3857ef147c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51769772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98932242e8c335fd35ffd6dc476fcb7622b6d05f0d49508e382566c0b14f1236`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:08 GMT
ADD file:e077f4d014ea0869fc4b3d5a3e6b3c8b792a97a8b4a328f33a994369225ff222 in / 
# Tue, 31 Mar 2020 01:24:08 GMT
CMD ["bash"]
# Mon, 06 Apr 2020 20:19:54 GMT
ENV AEROSPIKE_VERSION=4.7.0.12
# Mon, 06 Apr 2020 20:19:54 GMT
ENV AEROSPIKE_SHA256=9169014025e376cf53cdd7440cad18f1dffe02feaa3abd697383a7678870efe8
# Mon, 06 Apr 2020 20:20:10 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Mon, 06 Apr 2020 20:20:10 GMT
COPY file:b2afebdf574a22640dc0687630172a267f2dc7857e8cd93254039deab3b62213 in /etc/aerospike/aerospike.template.conf 
# Mon, 06 Apr 2020 20:20:11 GMT
COPY file:688bc1b7dea55c1dc5575a99640936049823d07bac5c920bbace2369fbb27428 in /entrypoint.sh 
# Mon, 06 Apr 2020 20:20:11 GMT
VOLUME [/opt/aerospike/data]
# Mon, 06 Apr 2020 20:20:11 GMT
EXPOSE 3000 3001 3002 3003
# Mon, 06 Apr 2020 20:20:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Apr 2020 20:20:11 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:48839397421a64189661c2b86a34eb515d09a28204587a2b06b59df9f6e2d786`  
		Last Modified: Tue, 31 Mar 2020 01:29:28 GMT  
		Size: 22.5 MB (22513374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8eabfb5467e067c4d6aaa9fa92b7f3959870ede017f53466c2337544dbff547`  
		Last Modified: Mon, 06 Apr 2020 20:21:00 GMT  
		Size: 29.3 MB (29254380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e574a99b8b5abf9cee6c9938e14915685fe9f13e5a64ce123504d9a6d034c11a`  
		Last Modified: Mon, 06 Apr 2020 20:20:53 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d391642ed04e4c6b581833435df9f4b7c85a3c941d1fd13b3d9512d1c417cb4e`  
		Last Modified: Mon, 06 Apr 2020 20:20:53 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:4.8.0.8`

```console
$ docker pull aerospike@sha256:35b760bff9e667957cfa8cf84a708054a369edb01c6c026aefd54f395f7c31d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:4.8.0.8` - linux; amd64

```console
$ docker pull aerospike@sha256:fa7148002aa3462b955fdd02b24a8bec666a362610991821ab9fc7c4ae1941d2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51846274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa12f3b4547044802cb4b1d2da2d5f9b3cedb53c8d7972ea3dfd4e59d63ff7db`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:08 GMT
ADD file:e077f4d014ea0869fc4b3d5a3e6b3c8b792a97a8b4a328f33a994369225ff222 in / 
# Tue, 31 Mar 2020 01:24:08 GMT
CMD ["bash"]
# Mon, 06 Apr 2020 20:20:18 GMT
ENV AEROSPIKE_VERSION=4.8.0.8
# Mon, 06 Apr 2020 20:20:18 GMT
ENV AEROSPIKE_SHA256=0239bb572069d4c803a5f558a4118c2dc7374ca539804fbc39a8d79101cf4e9e
# Mon, 06 Apr 2020 20:20:34 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Mon, 06 Apr 2020 20:20:34 GMT
COPY file:b2afebdf574a22640dc0687630172a267f2dc7857e8cd93254039deab3b62213 in /etc/aerospike/aerospike.template.conf 
# Mon, 06 Apr 2020 20:20:35 GMT
COPY file:688bc1b7dea55c1dc5575a99640936049823d07bac5c920bbace2369fbb27428 in /entrypoint.sh 
# Mon, 06 Apr 2020 20:20:35 GMT
VOLUME [/opt/aerospike/data]
# Mon, 06 Apr 2020 20:20:35 GMT
EXPOSE 3000 3001 3002 3003
# Mon, 06 Apr 2020 20:20:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Apr 2020 20:20:35 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:48839397421a64189661c2b86a34eb515d09a28204587a2b06b59df9f6e2d786`  
		Last Modified: Tue, 31 Mar 2020 01:29:28 GMT  
		Size: 22.5 MB (22513374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0507a6f2f524418c20cb5c52ca79a4ac9f3be0bb19451cf85b47702ab0903a8a`  
		Last Modified: Mon, 06 Apr 2020 20:21:08 GMT  
		Size: 29.3 MB (29330884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7edbd6426c9989b8a3350590a8d4c692aad4640fcba9191dd3293c311d4dda6`  
		Last Modified: Mon, 06 Apr 2020 20:21:03 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec4fc6a2dd147c52fe9fc71a32d142b2827d23832929a523e46cf000eaa484e`  
		Last Modified: Mon, 06 Apr 2020 20:21:03 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:latest`

```console
$ docker pull aerospike@sha256:35b760bff9e667957cfa8cf84a708054a369edb01c6c026aefd54f395f7c31d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:fa7148002aa3462b955fdd02b24a8bec666a362610991821ab9fc7c4ae1941d2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51846274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa12f3b4547044802cb4b1d2da2d5f9b3cedb53c8d7972ea3dfd4e59d63ff7db`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:08 GMT
ADD file:e077f4d014ea0869fc4b3d5a3e6b3c8b792a97a8b4a328f33a994369225ff222 in / 
# Tue, 31 Mar 2020 01:24:08 GMT
CMD ["bash"]
# Mon, 06 Apr 2020 20:20:18 GMT
ENV AEROSPIKE_VERSION=4.8.0.8
# Mon, 06 Apr 2020 20:20:18 GMT
ENV AEROSPIKE_SHA256=0239bb572069d4c803a5f558a4118c2dc7374ca539804fbc39a8d79101cf4e9e
# Mon, 06 Apr 2020 20:20:34 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Mon, 06 Apr 2020 20:20:34 GMT
COPY file:b2afebdf574a22640dc0687630172a267f2dc7857e8cd93254039deab3b62213 in /etc/aerospike/aerospike.template.conf 
# Mon, 06 Apr 2020 20:20:35 GMT
COPY file:688bc1b7dea55c1dc5575a99640936049823d07bac5c920bbace2369fbb27428 in /entrypoint.sh 
# Mon, 06 Apr 2020 20:20:35 GMT
VOLUME [/opt/aerospike/data]
# Mon, 06 Apr 2020 20:20:35 GMT
EXPOSE 3000 3001 3002 3003
# Mon, 06 Apr 2020 20:20:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Apr 2020 20:20:35 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:48839397421a64189661c2b86a34eb515d09a28204587a2b06b59df9f6e2d786`  
		Last Modified: Tue, 31 Mar 2020 01:29:28 GMT  
		Size: 22.5 MB (22513374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0507a6f2f524418c20cb5c52ca79a4ac9f3be0bb19451cf85b47702ab0903a8a`  
		Last Modified: Mon, 06 Apr 2020 20:21:08 GMT  
		Size: 29.3 MB (29330884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7edbd6426c9989b8a3350590a8d4c692aad4640fcba9191dd3293c311d4dda6`  
		Last Modified: Mon, 06 Apr 2020 20:21:03 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec4fc6a2dd147c52fe9fc71a32d142b2827d23832929a523e46cf000eaa484e`  
		Last Modified: Mon, 06 Apr 2020 20:21:03 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
