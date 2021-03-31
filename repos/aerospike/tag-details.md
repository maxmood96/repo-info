<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:5.3.0.10`](#aerospike53010)
-	[`aerospike:5.4.0.5`](#aerospike5405)
-	[`aerospike:5.5.0.3`](#aerospike5503)
-	[`aerospike:latest`](#aerospikelatest)

## `aerospike:5.3.0.10`

```console
$ docker pull aerospike@sha256:7c8aedad9e5446d2bab6b730122d57ee23e0925ccd784bcdc6a35b5d36ca6946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.3.0.10` - linux; amd64

```console
$ docker pull aerospike@sha256:6f12d2c1b20c872cea6418d80eba4f383573f51a2aa2ee11afdfd1cbadefe035
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74717545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1700d2287f824c39e4d3f437b824bd9c1937166e08710038265262f7ceb3be4`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:55 GMT
ADD file:65a51da79ba9e2993b794078e3e24554bff59ac80185f12845c1426c7173f06f in / 
# Tue, 30 Mar 2021 21:50:55 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 11:42:06 GMT
ENV AEROSPIKE_VERSION=5.3.0.10
# Wed, 31 Mar 2021 11:42:06 GMT
ENV AEROSPIKE_SHA256=d05e9db2936fda4e29fdd6bd3115f98c96f3c3eda22b1328f735869520b34307
# Wed, 31 Mar 2021 11:42:27 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Wed, 31 Mar 2021 11:42:28 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Wed, 31 Mar 2021 11:42:28 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Wed, 31 Mar 2021 11:42:28 GMT
EXPOSE 3000 3001 3002 3003
# Wed, 31 Mar 2021 11:42:28 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Wed, 31 Mar 2021 11:42:29 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:23a3602cd30cf5ce6da03e18c28bbbfdc12ae98f182462de8c55785a8d982431`  
		Last Modified: Tue, 30 Mar 2021 21:57:04 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df43e98683f2cab285ee04e22901438a4a411fb8abea08785d0ba234cca9019`  
		Last Modified: Wed, 31 Mar 2021 11:44:00 GMT  
		Size: 52.2 MB (52187229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7495d4c7f4ddbb06b76074ba59f4dea9c7c1352ae495fc60635fbd2e3a24f36`  
		Last Modified: Wed, 31 Mar 2021 11:43:46 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd87b62464077d7b952569947d97f3f86f2c8a862c6672041f3a7f97fbf5fc86`  
		Last Modified: Wed, 31 Mar 2021 11:43:46 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:5.4.0.5`

```console
$ docker pull aerospike@sha256:230bd20858d658992ed71e8f2ca4e0130583c2cd7faab965accdb88f053044b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.4.0.5` - linux; amd64

```console
$ docker pull aerospike@sha256:2a66648ba6278b5142d0b6ad1b5aa6f3c5aa5f6eb1b525510c324a031c41e57e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74736806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3352ef3a27148d156b4a0c04ec0d83403ac6de45af1afb3a85f7f84dc7e3eacb`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:55 GMT
ADD file:65a51da79ba9e2993b794078e3e24554bff59ac80185f12845c1426c7173f06f in / 
# Tue, 30 Mar 2021 21:50:55 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 11:42:32 GMT
ENV AEROSPIKE_VERSION=5.4.0.5
# Wed, 31 Mar 2021 11:42:32 GMT
ENV AEROSPIKE_SHA256=a30f09784dfa4dda36af633210b43cda493663d2faedac87b8b27aa4f60d0231
# Wed, 31 Mar 2021 11:42:53 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Wed, 31 Mar 2021 11:42:54 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Wed, 31 Mar 2021 11:42:54 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Wed, 31 Mar 2021 11:42:54 GMT
EXPOSE 3000 3001 3002 3003
# Wed, 31 Mar 2021 11:42:54 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Wed, 31 Mar 2021 11:42:55 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:23a3602cd30cf5ce6da03e18c28bbbfdc12ae98f182462de8c55785a8d982431`  
		Last Modified: Tue, 30 Mar 2021 21:57:04 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77033022df7e547e3ea4f8de9d38d9aa0d7b778c532365b489b705cab4e29ed7`  
		Last Modified: Wed, 31 Mar 2021 11:44:22 GMT  
		Size: 52.2 MB (52206487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1d4af51c54324d320be1239e12f959281797b7c31d37fb370433c60278f25c`  
		Last Modified: Wed, 31 Mar 2021 11:44:11 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbcdf936fc8e78fcff118b28e0734286ebaefa0c3c45a9e72872166551c5d10b`  
		Last Modified: Wed, 31 Mar 2021 11:44:11 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:5.5.0.3`

```console
$ docker pull aerospike@sha256:0a68ab9d4899975b8d0ef0a575930157e5119691f389a24e5c28a56dc39d1588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:5.5.0.3` - linux; amd64

```console
$ docker pull aerospike@sha256:4c3059d77dc5e0e3d5227c05a9f073388c4ae282a94ac29a0d35b991f521ff29
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74775628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:682ab7896f446e173aaf1e6412c79188d2dbd8bd3c86e6c305166721303d1f01`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:55 GMT
ADD file:65a51da79ba9e2993b794078e3e24554bff59ac80185f12845c1426c7173f06f in / 
# Tue, 30 Mar 2021 21:50:55 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 11:42:57 GMT
ENV AEROSPIKE_VERSION=5.5.0.3
# Wed, 31 Mar 2021 11:42:58 GMT
ENV AEROSPIKE_SHA256=5649c59750042c8926af6ea2120a9ce6de008e9e4fede1329735b32a82f6dec2
# Wed, 31 Mar 2021 11:43:23 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Wed, 31 Mar 2021 11:43:24 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Wed, 31 Mar 2021 11:43:25 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Wed, 31 Mar 2021 11:43:25 GMT
EXPOSE 3000 3001 3002 3003
# Wed, 31 Mar 2021 11:43:26 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Wed, 31 Mar 2021 11:43:26 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:23a3602cd30cf5ce6da03e18c28bbbfdc12ae98f182462de8c55785a8d982431`  
		Last Modified: Tue, 30 Mar 2021 21:57:04 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432c88e9d7875be126fb9178da9b7e980ef157f7571004ec30de8be72f4fe4f7`  
		Last Modified: Wed, 31 Mar 2021 11:44:41 GMT  
		Size: 52.2 MB (52245312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04eb40d59199a0db59e96fd698c96d39471f870a6ab442a245b41e85e5fafb95`  
		Last Modified: Wed, 31 Mar 2021 11:44:31 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0d2d211cd4bb708d5b84970bb82f72616eca6d9a86c78574d5d6350843d5b4`  
		Last Modified: Wed, 31 Mar 2021 11:44:31 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:latest`

```console
$ docker pull aerospike@sha256:0a68ab9d4899975b8d0ef0a575930157e5119691f389a24e5c28a56dc39d1588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:4c3059d77dc5e0e3d5227c05a9f073388c4ae282a94ac29a0d35b991f521ff29
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74775628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:682ab7896f446e173aaf1e6412c79188d2dbd8bd3c86e6c305166721303d1f01`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:55 GMT
ADD file:65a51da79ba9e2993b794078e3e24554bff59ac80185f12845c1426c7173f06f in / 
# Tue, 30 Mar 2021 21:50:55 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 11:42:57 GMT
ENV AEROSPIKE_VERSION=5.5.0.3
# Wed, 31 Mar 2021 11:42:58 GMT
ENV AEROSPIKE_SHA256=5649c59750042c8926af6ea2120a9ce6de008e9e4fede1329735b32a82f6dec2
# Wed, 31 Mar 2021 11:43:23 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Wed, 31 Mar 2021 11:43:24 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Wed, 31 Mar 2021 11:43:25 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Wed, 31 Mar 2021 11:43:25 GMT
EXPOSE 3000 3001 3002 3003
# Wed, 31 Mar 2021 11:43:26 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Wed, 31 Mar 2021 11:43:26 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:23a3602cd30cf5ce6da03e18c28bbbfdc12ae98f182462de8c55785a8d982431`  
		Last Modified: Tue, 30 Mar 2021 21:57:04 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432c88e9d7875be126fb9178da9b7e980ef157f7571004ec30de8be72f4fe4f7`  
		Last Modified: Wed, 31 Mar 2021 11:44:41 GMT  
		Size: 52.2 MB (52245312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04eb40d59199a0db59e96fd698c96d39471f870a6ab442a245b41e85e5fafb95`  
		Last Modified: Wed, 31 Mar 2021 11:44:31 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0d2d211cd4bb708d5b84970bb82f72616eca6d9a86c78574d5d6350843d5b4`  
		Last Modified: Wed, 31 Mar 2021 11:44:31 GMT  
		Size: 897.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
