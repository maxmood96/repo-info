<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:4.8.0.11`](#aerospike48011)
-	[`aerospike:4.9.0.8`](#aerospike4908)
-	[`aerospike:5.0.0.4`](#aerospike5004)
-	[`aerospike:latest`](#aerospikelatest)

## `aerospike:4.8.0.11`

**does not exist** (yet?)

## `aerospike:4.9.0.8`

**does not exist** (yet?)

## `aerospike:5.0.0.4`

**does not exist** (yet?)

## `aerospike:latest`

```console
$ docker pull aerospike@sha256:2d6e80246e17e3dc12a9fd115e903e343e3c9650bf8b337947233f0f531dfbac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:373d7c130166ba64e4ed0a1f48328bcced9db0b63e5298e7b7f21968ba66e98f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53089989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ec378e8545a6416e27ed38f0747abb7a5a053981fcb783de2e381f917ac3c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Fri, 15 May 2020 06:33:44 GMT
ADD file:ff87497c2a2fce1d776e432139030782373ac1549522a8366694786b45387306 in / 
# Fri, 15 May 2020 06:33:44 GMT
CMD ["bash"]
# Sat, 16 May 2020 09:59:54 GMT
ENV AEROSPIKE_VERSION=5.0.0.3
# Sat, 16 May 2020 09:59:54 GMT
ENV AEROSPIKE_SHA256=024ebdd12d0088450a910d1eaa05685d03bf5762cafd4752fc59409a4534dc15
# Sat, 16 May 2020 10:00:11 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Sat, 16 May 2020 10:00:12 GMT
COPY file:e804504afb5c4e22745b04c055979dfb9d5529cb7405e101861ade614def86f5 in /etc/aerospike/aerospike.template.conf 
# Sat, 16 May 2020 10:00:12 GMT
COPY file:51ea788984274d9d596ae7f174fc5d76048404a3be1d56d9df20cec477707497 in /entrypoint.sh 
# Sat, 16 May 2020 10:00:12 GMT
VOLUME [/opt/aerospike/data]
# Sat, 16 May 2020 10:00:12 GMT
EXPOSE 3000 3001 3002 3003
# Sat, 16 May 2020 10:00:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 May 2020 10:00:12 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:e62d08fa1eb18131b4109c7cbece97f4f7e37d6ea09845a21beb3a899d0c963d`  
		Last Modified: Fri, 15 May 2020 06:40:45 GMT  
		Size: 22.5 MB (22519887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3803b6657925020d950deb15c3e46603aba89e31dfe8a0930447c29e9d446c3e`  
		Last Modified: Sat, 16 May 2020 10:00:38 GMT  
		Size: 30.6 MB (30568049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5471d43ff27912d2be7280e4f85aed131d00a004c0ea4e6cbfd5c6303c27c7`  
		Last Modified: Sat, 16 May 2020 10:00:33 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520388c565fca8f3a80c46b5e1abbf085af875a08d2f168b31dcd4b3ae7cf500`  
		Last Modified: Sat, 16 May 2020 10:00:33 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
