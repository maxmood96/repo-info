<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:ce-5.6.0.7`](#aerospikece-5607)
-	[`aerospike:ee-5.6.0.7`](#aerospikeee-5607)

## `aerospike:ce-5.6.0.7`

```console
$ docker pull aerospike@sha256:43476762c5bb049299cb4706c8bcf8ffd59c9bb416066863988f96a9b6e2b9a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:ce-5.6.0.7` - linux; amd64

```console
$ docker pull aerospike@sha256:455887bc63b4ad4e25bdac0e50f6cec200eabc5c92029f38263e63dc8c7af994
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80606651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15a1abb6781d7ab3913e0335596cd5031dbddef7d98cf23fb42f59c4564e2fa`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 07 Jul 2021 20:22:16 GMT
ENV AEROSPIKE_VERSION=5.6.0.7
# Wed, 07 Jul 2021 20:22:47 GMT
ENV AEROSPIKE_SHA256=a8693ee9eae5e818828066c0a091cb5cf0c2795c548308948582c2f7f04942ca
# Wed, 07 Jul 2021 20:23:09 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Wed, 07 Jul 2021 20:23:09 GMT
COPY file:1897c4aae07efbc61bf2d8c2c7b0dfb0990174e11cc787eac71d5adf767abaed in /etc/aerospike/aerospike.template.conf 
# Wed, 07 Jul 2021 20:23:10 GMT
COPY file:e1d47057fdb4c34c118f7ba5898161c386b475cba70907a4ae483866cf07335b in /entrypoint.sh 
# Wed, 07 Jul 2021 20:23:10 GMT
EXPOSE 3000 3001 3002
# Wed, 07 Jul 2021 20:23:10 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Wed, 07 Jul 2021 20:23:10 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c076e27d996cca18e9fd30de8e677b317841bc0814cc44e6e87f24083fa909a6`  
		Last Modified: Wed, 07 Jul 2021 20:23:49 GMT  
		Size: 53.5 MB (53458780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa65f0ae5ee586f130e91622896e9bd2704824350bb8026f552fdd5cfcb952e0`  
		Last Modified: Wed, 07 Jul 2021 20:23:40 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81737fb7f60da40921cbeac732a97cbaacff52b4f03595dd95e06c86021b05f6`  
		Last Modified: Wed, 07 Jul 2021 20:23:40 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:ee-5.6.0.7`

```console
$ docker pull aerospike@sha256:5328c6e57b09089aa2f172600ffb72fb9e2163f69aab9f3225baefc6a89f608c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:ee-5.6.0.7` - linux; amd64

```console
$ docker pull aerospike@sha256:c68dc2a2511ff625ea8dd873d2ceae3a16f4a9db7ae32efc7714f7278971bac7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82472404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3df43bd9577ffce0253a818f4d3b08412442199286e25478764354f0afb72b85`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Wed, 23 Jun 2021 00:20:40 GMT
ADD file:4903a19c327468b0e08e4f463cfc162c66b85b4618b5803d71365862f6302e0b in / 
# Wed, 23 Jun 2021 00:20:40 GMT
CMD ["bash"]
# Wed, 07 Jul 2021 20:22:16 GMT
ENV AEROSPIKE_VERSION=5.6.0.7
# Wed, 07 Jul 2021 20:22:17 GMT
ENV AEROSPIKE_SHA256=73ef48026c53faf0158c6fe26994fb8309ebcbf27e03fe0837b74510626014c1
# Wed, 07 Jul 2021 20:22:40 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libldap-dev libcurl4-openssl-dev   && wget "https://www.aerospike.com/enterprise/download/server/${AEROSPIKE_VERSION}/artifact/debian10" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Wed, 07 Jul 2021 20:22:41 GMT
COPY file:7d75174e09b209cf7f56b715636c2b8e08dd083d548e8cdc8517cabd512600b5 in /etc/aerospike/aerospike.template.conf 
# Wed, 07 Jul 2021 20:22:41 GMT
COPY file:31b6a51a1d9d91f22433472f07f6ddfe3cea3bb07f460dd69c4187bc7fd20fdf in /entrypoint.sh 
# Wed, 07 Jul 2021 20:22:41 GMT
EXPOSE 3000 3001 3002
# Wed, 07 Jul 2021 20:22:41 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Wed, 07 Jul 2021 20:22:41 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:b4d181a07f8025e00e0cb28f1cc14613da2ce26450b80c54aea537fa93cf3bda`  
		Last Modified: Wed, 23 Jun 2021 00:25:39 GMT  
		Size: 27.1 MB (27145851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1db87b8535f04b03338462f11df40989d680bfe92f5caea41391ab85b6ef47`  
		Last Modified: Wed, 07 Jul 2021 20:23:32 GMT  
		Size: 55.3 MB (55324473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6098cc596e9d2e7bfb9ef6b7e075cb36f398beb5fe4f5cfd144ab4b6befbcea9`  
		Last Modified: Wed, 07 Jul 2021 20:23:23 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cbd8bb20a49cf5bf50b980148297efa9e9228eae85cf002e858d9cb835a5b51`  
		Last Modified: Wed, 07 Jul 2021 20:23:23 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
