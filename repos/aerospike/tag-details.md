<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:4.7.0.13`](#aerospike47013)
-	[`aerospike:4.8.0.9`](#aerospike4809)
-	[`aerospike:latest`](#aerospikelatest)

## `aerospike:4.7.0.13`

**does not exist** (yet?)

## `aerospike:4.8.0.9`

**does not exist** (yet?)

## `aerospike:latest`

```console
$ docker pull aerospike@sha256:b6b40e3568816258ef9175d06093a59337bdbe18751d519b49556888234907c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:7915bb4e46d2e279b0a5cb2951ba21679b2a6c5aa9311a0d5072fc808da474cc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53186870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aad73c3f9e20bb385f374b4caf7742e3d7db82a4f38ef8e1b3404f89f2f2c03`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:50 GMT
ADD file:40f52c233aecabf572a9db7450590d54d5e125fb00ecbb4a26fecd0b71e84eb8 in / 
# Thu, 16 Apr 2020 03:27:50 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 04:22:36 GMT
ENV AEROSPIKE_VERSION=4.9.0.3
# Thu, 16 Apr 2020 04:22:36 GMT
ENV AEROSPIKE_SHA256=25247f67b4be624d46892dd1a66d945fafe1500107dd6cbf386dbc57e8816fb1
# Thu, 16 Apr 2020 04:22:54 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Thu, 16 Apr 2020 04:22:55 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Thu, 16 Apr 2020 04:22:55 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Thu, 16 Apr 2020 04:22:55 GMT
VOLUME [/opt/aerospike/data]
# Thu, 16 Apr 2020 04:22:55 GMT
EXPOSE 3000 3001 3002 3003
# Thu, 16 Apr 2020 04:22:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Apr 2020 04:22:56 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:5e35bd43cf7898d036f8515be74d45b2e3abd2a5534fc280de63a9c22dd175bd`  
		Last Modified: Thu, 16 Apr 2020 03:35:04 GMT  
		Size: 22.5 MB (22513476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554195f11b8034f38d7be796bc6da3828644dee8d6d21c2496bc7a97b879f19f`  
		Last Modified: Thu, 16 Apr 2020 04:23:46 GMT  
		Size: 30.7 MB (30671339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcbb76112010ae06b66e51300b5b5f7696818f9d577b0eba13fab9cda7855d3`  
		Last Modified: Thu, 16 Apr 2020 04:23:38 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:badeb8f0ff3666a75a9425028bde0ac1b2a7d2103185722efe7627c308c35dd0`  
		Last Modified: Thu, 16 Apr 2020 04:23:38 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
