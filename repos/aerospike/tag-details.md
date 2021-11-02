<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:ce-5.7.0.8`](#aerospikece-5708)
-	[`aerospike:ee-5.7.0.8`](#aerospikeee-5708)

## `aerospike:ce-5.7.0.8`

```console
$ docker pull aerospike@sha256:958a925cbc8e0510a4a446aab5192e94336081f5591fcd44e00d7ccb542e65a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ce-5.7.0.8` - linux; amd64

```console
$ docker pull aerospike@sha256:5e8c923b30261d583464309b5dd9b94ebfc71794697057e606847c2ce48599ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81519473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6baaef46f041f1876348bd30d17b6a5e884add7bd5a69b3e0a848b18152acf8`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 02 Nov 2021 20:19:19 GMT
ENV AEROSPIKE_VERSION=5.7.0.8
# Tue, 02 Nov 2021 20:19:47 GMT
ENV AEROSPIKE_SHA256=587baea6f9ff594ae168a1dd21becccfd9cf4298cb073bb6f13e0ca72b6c42c0
# Tue, 02 Nov 2021 20:20:06 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Tue, 02 Nov 2021 20:20:06 GMT
COPY file:1897c4aae07efbc61bf2d8c2c7b0dfb0990174e11cc787eac71d5adf767abaed in /etc/aerospike/aerospike.template.conf 
# Tue, 02 Nov 2021 20:20:06 GMT
COPY file:e1d47057fdb4c34c118f7ba5898161c386b475cba70907a4ae483866cf07335b in /entrypoint.sh 
# Tue, 02 Nov 2021 20:20:07 GMT
EXPOSE 3000 3001 3002
# Tue, 02 Nov 2021 20:20:07 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Tue, 02 Nov 2021 20:20:07 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8296f51dc89b6928634a4b3f10889c66264ef0db27bfb6e7c42b60467f39707f`  
		Last Modified: Tue, 02 Nov 2021 20:20:38 GMT  
		Size: 54.4 MB (54377944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a91acbab8953c63b58864b7c5d72b0a4878c8d9125f8c38cab39c274361504`  
		Last Modified: Tue, 02 Nov 2021 20:20:30 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02db796c26efd1963c7be4e7220ea7c220df6562a8b6e581e19bae59c6013dad`  
		Last Modified: Tue, 02 Nov 2021 20:20:30 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:ee-5.7.0.8`

```console
$ docker pull aerospike@sha256:d2f25676a1f990d477eef3e086ea82ad8bbba4b738ea4ef0cc60e0a076de75ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ee-5.7.0.8` - linux; amd64

```console
$ docker pull aerospike@sha256:c434095c5264375fce150ccf590db7a8330a4666fad7dd35621c6de02bd76fd6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83517775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e81246383e88d1905b45b1d12ab84decb223b2d9340bd7d7e179fe76557cd65`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 02 Nov 2021 20:19:19 GMT
ENV AEROSPIKE_VERSION=5.7.0.8
# Tue, 02 Nov 2021 20:19:19 GMT
ENV AEROSPIKE_SHA256=cb3e0c376ae4be9253fa4e44a005599684bf2aec66211fae87edab20b56eed0a
# Tue, 02 Nov 2021 20:19:41 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libldap-dev libcurl4-openssl-dev   && wget "https://www.aerospike.com/enterprise/download/server/${AEROSPIKE_VERSION}/artifact/debian10" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Tue, 02 Nov 2021 20:19:41 GMT
COPY file:7d75174e09b209cf7f56b715636c2b8e08dd083d548e8cdc8517cabd512600b5 in /etc/aerospike/aerospike.template.conf 
# Tue, 02 Nov 2021 20:19:41 GMT
COPY file:31b6a51a1d9d91f22433472f07f6ddfe3cea3bb07f460dd69c4187bc7fd20fdf in /entrypoint.sh 
# Tue, 02 Nov 2021 20:19:42 GMT
EXPOSE 3000 3001 3002
# Tue, 02 Nov 2021 20:19:42 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Tue, 02 Nov 2021 20:19:42 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e839eeb33013f922d4fcf18ac7594aafd8ca36dea37b751b42dd0d790bb71e6`  
		Last Modified: Tue, 02 Nov 2021 20:20:23 GMT  
		Size: 56.4 MB (56376184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503da19ac9ee459960627c8abcb6cdcde6e62ab2755b0dd8ce19d82cb42ca5e1`  
		Last Modified: Tue, 02 Nov 2021 20:20:15 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f48a36fd247d5a29087a5d1eb1f080c2de41515df5f0302ab77ee315186196`  
		Last Modified: Tue, 02 Nov 2021 20:20:15 GMT  
		Size: 909.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
