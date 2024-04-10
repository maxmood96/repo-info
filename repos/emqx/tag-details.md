<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:5`](#emqx5)
-	[`emqx:5.1`](#emqx51)
-	[`emqx:5.1.6`](#emqx516)
-	[`emqx:5.2`](#emqx52)
-	[`emqx:5.2.1`](#emqx521)
-	[`emqx:5.3`](#emqx53)
-	[`emqx:5.3.2`](#emqx532)
-	[`emqx:5.4`](#emqx54)
-	[`emqx:5.4.1`](#emqx541)
-	[`emqx:5.5`](#emqx55)
-	[`emqx:5.5.1`](#emqx551)
-	[`emqx:5.6`](#emqx56)
-	[`emqx:5.6.0`](#emqx560)
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:eeb7d4644febb2653ebc0e8af835f5022012e46e912af42e4259914734c15a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:2842db71854f230d76883f41a4c85e00164909c29a40cfc52947cfe2ebad2a0c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (121967256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e156bccc4eee382f32c9b0db5ccd573f2490d83968c4fff7277d6d675f5b1de4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:10:59 GMT
ENV EMQX_VERSION=5.6.0
# Wed, 10 Apr 2024 07:10:59 GMT
ENV AMD64_SHA256=d04535234c91dada9ae794247ccc70139c980c24a2f4609e8253c95e75b992ec
# Wed, 10 Apr 2024 07:10:59 GMT
ENV ARM64_SHA256=c40a6f7a70fce3874a4db804cb908f808a0119d77d1db324bdf3050b7429f31d
# Wed, 10 Apr 2024 07:10:59 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 07:11:16 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     apt-get clean;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 10 Apr 2024 07:11:16 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 07:11:16 GMT
USER emqx
# Wed, 10 Apr 2024 07:11:16 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 07:11:16 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 07:11:17 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Wed, 10 Apr 2024 07:11:17 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 07:11:17 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97bd7388580f03db39cddd67403c46b04e503642fb9c7c08290acf9e397edd5`  
		Last Modified: Wed, 10 Apr 2024 07:13:01 GMT  
		Size: 92.8 MB (92834864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2e141b774b38a6b8c7b8afd956fc6432a04b878c2a483b4c378d605bd38dd5`  
		Last Modified: Wed, 10 Apr 2024 07:12:52 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:f5738e10c2c3ed991760301957d2405565903fa29b7610796e1c9e229a2a4e1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.6 MB (118551298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43892ef99d6270cdd081b4916b189c2ae090cdcef53ad86b37a597e69e40acd`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Thu, 04 Apr 2024 20:05:11 GMT
ENV EMQX_VERSION=5.6.0
# Thu, 04 Apr 2024 20:05:11 GMT
ENV AMD64_SHA256=d04535234c91dada9ae794247ccc70139c980c24a2f4609e8253c95e75b992ec
# Thu, 04 Apr 2024 20:05:11 GMT
ENV ARM64_SHA256=c40a6f7a70fce3874a4db804cb908f808a0119d77d1db324bdf3050b7429f31d
# Thu, 04 Apr 2024 20:05:11 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 04 Apr 2024 20:05:26 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     apt-get clean;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 04 Apr 2024 20:05:27 GMT
WORKDIR /opt/emqx
# Thu, 04 Apr 2024 20:05:27 GMT
USER emqx
# Thu, 04 Apr 2024 20:05:27 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 04 Apr 2024 20:05:27 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 04 Apr 2024 20:05:27 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Thu, 04 Apr 2024 20:05:27 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 04 Apr 2024 20:05:27 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f35daaece97c1436bc272e916d8f54078b821e6e9c6fa5215c425c72c9def82`  
		Last Modified: Thu, 04 Apr 2024 20:06:13 GMT  
		Size: 89.4 MB (89393828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8171ff5cb00ca906ec69033298157d6f15a528cc1f6450cea2b0f7ab4a73176`  
		Last Modified: Thu, 04 Apr 2024 20:06:05 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1`

```console
$ docker pull emqx@sha256:bd7b12abbe95219e21d6dabcf4a54c81dc95d6f82329465323bea76fbd677dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1` - linux; amd64

```console
$ docker pull emqx@sha256:0643ee036a68c68147288e58613e595e5e5ccc4338d8f834d50bcd14c6008363
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102402310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76180abb30b2557a88028bcf792b092096879c3daea9071052e8254a7f1d244b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:09:22 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:09:23 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 10 Apr 2024 07:09:23 GMT
ENV EMQX_VERSION=5.1.6
# Wed, 10 Apr 2024 07:09:23 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Wed, 10 Apr 2024 07:09:23 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Wed, 10 Apr 2024 07:09:23 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 07:09:30 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Wed, 10 Apr 2024 07:09:31 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 07:09:31 GMT
USER emqx
# Wed, 10 Apr 2024 07:09:31 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 07:09:31 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 07:09:31 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 10 Apr 2024 07:09:31 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 07:09:31 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb75347c57d452dccf220e908f0594851a6a0af43ebc5cdbc2218cbb7b8e045`  
		Last Modified: Wed, 10 Apr 2024 07:11:30 GMT  
		Size: 3.0 MB (2988332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e37a9e4690a29cfeaf903962d665f4dcf7f9cec23880039e62e3fb4e3c7ef9`  
		Last Modified: Wed, 10 Apr 2024 07:11:30 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15ae4f84de9e5883c178ab5efae48ce4bc4fae3560e9a2dca47dd3103acd765`  
		Last Modified: Wed, 10 Apr 2024 07:11:37 GMT  
		Size: 68.0 MB (67981233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77fb989d7d6376a44f9adaa549cb50e768fadd243db9827b1cad74ee3898c97`  
		Last Modified: Wed, 10 Apr 2024 07:11:30 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8430c3e61b2ce88fd1bf4c3d13013a0ff5ab1334b25c89e19aea8d7291d71a85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92705262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4105a9afd5fa2b537ca291cc22add0fa514606aa521eda21a545a38589e253`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:17:15 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:17:15 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 12 Mar 2024 02:17:15 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 12 Mar 2024 02:17:15 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 12 Mar 2024 02:17:15 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 12 Mar 2024 02:17:16 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 12 Mar 2024 02:17:22 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 12 Mar 2024 02:17:22 GMT
WORKDIR /opt/emqx
# Tue, 12 Mar 2024 02:17:22 GMT
USER emqx
# Tue, 12 Mar 2024 02:17:22 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 12 Mar 2024 02:17:22 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 12 Mar 2024 02:17:23 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 12 Mar 2024 02:17:23 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 02:17:23 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a62f034509794d0cf59e746308fc478c3a222b3f0be4cc504626f5b78c8b4fd`  
		Last Modified: Tue, 12 Mar 2024 02:18:39 GMT  
		Size: 3.0 MB (3004435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50ea762249680868d468b0e66c29c185fe47e7f113bda1519ac5a6f673c95bd`  
		Last Modified: Tue, 12 Mar 2024 02:18:39 GMT  
		Size: 4.1 KB (4112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf339c734d137af79597212523518989d1182f754a2275a118984f60f06a9f1`  
		Last Modified: Tue, 12 Mar 2024 02:18:44 GMT  
		Size: 59.6 MB (59624698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b69a662bfe25b7b221b62dbb20d8f9c9b493e77bb1bb34bc3d35142ab3766de`  
		Last Modified: Tue, 12 Mar 2024 02:18:39 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1.6`

```console
$ docker pull emqx@sha256:bd7b12abbe95219e21d6dabcf4a54c81dc95d6f82329465323bea76fbd677dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1.6` - linux; amd64

```console
$ docker pull emqx@sha256:0643ee036a68c68147288e58613e595e5e5ccc4338d8f834d50bcd14c6008363
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102402310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76180abb30b2557a88028bcf792b092096879c3daea9071052e8254a7f1d244b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:09:22 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:09:23 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 10 Apr 2024 07:09:23 GMT
ENV EMQX_VERSION=5.1.6
# Wed, 10 Apr 2024 07:09:23 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Wed, 10 Apr 2024 07:09:23 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Wed, 10 Apr 2024 07:09:23 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 07:09:30 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Wed, 10 Apr 2024 07:09:31 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 07:09:31 GMT
USER emqx
# Wed, 10 Apr 2024 07:09:31 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 07:09:31 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 07:09:31 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 10 Apr 2024 07:09:31 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 07:09:31 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb75347c57d452dccf220e908f0594851a6a0af43ebc5cdbc2218cbb7b8e045`  
		Last Modified: Wed, 10 Apr 2024 07:11:30 GMT  
		Size: 3.0 MB (2988332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e37a9e4690a29cfeaf903962d665f4dcf7f9cec23880039e62e3fb4e3c7ef9`  
		Last Modified: Wed, 10 Apr 2024 07:11:30 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15ae4f84de9e5883c178ab5efae48ce4bc4fae3560e9a2dca47dd3103acd765`  
		Last Modified: Wed, 10 Apr 2024 07:11:37 GMT  
		Size: 68.0 MB (67981233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77fb989d7d6376a44f9adaa549cb50e768fadd243db9827b1cad74ee3898c97`  
		Last Modified: Wed, 10 Apr 2024 07:11:30 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.1.6` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8430c3e61b2ce88fd1bf4c3d13013a0ff5ab1334b25c89e19aea8d7291d71a85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92705262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4105a9afd5fa2b537ca291cc22add0fa514606aa521eda21a545a38589e253`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:17:15 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:17:15 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 12 Mar 2024 02:17:15 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 12 Mar 2024 02:17:15 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 12 Mar 2024 02:17:15 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 12 Mar 2024 02:17:16 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 12 Mar 2024 02:17:22 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 12 Mar 2024 02:17:22 GMT
WORKDIR /opt/emqx
# Tue, 12 Mar 2024 02:17:22 GMT
USER emqx
# Tue, 12 Mar 2024 02:17:22 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 12 Mar 2024 02:17:22 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 12 Mar 2024 02:17:23 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 12 Mar 2024 02:17:23 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 02:17:23 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a62f034509794d0cf59e746308fc478c3a222b3f0be4cc504626f5b78c8b4fd`  
		Last Modified: Tue, 12 Mar 2024 02:18:39 GMT  
		Size: 3.0 MB (3004435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50ea762249680868d468b0e66c29c185fe47e7f113bda1519ac5a6f673c95bd`  
		Last Modified: Tue, 12 Mar 2024 02:18:39 GMT  
		Size: 4.1 KB (4112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf339c734d137af79597212523518989d1182f754a2275a118984f60f06a9f1`  
		Last Modified: Tue, 12 Mar 2024 02:18:44 GMT  
		Size: 59.6 MB (59624698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b69a662bfe25b7b221b62dbb20d8f9c9b493e77bb1bb34bc3d35142ab3766de`  
		Last Modified: Tue, 12 Mar 2024 02:18:39 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.2`

```console
$ docker pull emqx@sha256:4f0602463b4ba3183639e513744d8f9c1b71722c001d0946301ffb6739c48bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.2` - linux; amd64

```console
$ docker pull emqx@sha256:c7842d4a63d6f2ac6d385f714f382c5ee2a63b4454840674814a6abda6bfc4cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101172431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02cf8be8d7d1856c4cb09c41522e9d94fa6f4da7038b735cd19a94c251a09748`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:09:41 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:09:42 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 10 Apr 2024 07:09:42 GMT
ENV EMQX_VERSION=5.2.1
# Wed, 10 Apr 2024 07:09:42 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Wed, 10 Apr 2024 07:09:42 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Wed, 10 Apr 2024 07:09:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 07:09:53 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Wed, 10 Apr 2024 07:09:54 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 07:09:54 GMT
USER emqx
# Wed, 10 Apr 2024 07:09:54 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 07:09:54 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 07:09:54 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 10 Apr 2024 07:09:54 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 07:09:54 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659bee472f61e6a5c34eeeeb6b52574444c8f0f00fee74a8d7647be4feec6332`  
		Last Modified: Wed, 10 Apr 2024 07:11:47 GMT  
		Size: 1.6 MB (1629581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e3164039a5500ecd1b07faccf899e4c31871251f9733ec1948fc78fe32e305`  
		Last Modified: Wed, 10 Apr 2024 07:11:46 GMT  
		Size: 4.1 KB (4100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0db93238eabe5784aacd12eb497a576d4b67a8f47b2b042c2e8157f463086d6`  
		Last Modified: Wed, 10 Apr 2024 07:11:53 GMT  
		Size: 68.1 MB (68110109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a22bc1c301f31f63c12ddb59c936825db2a363474fbad4e8a497997d838905`  
		Last Modified: Wed, 10 Apr 2024 07:11:46 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:398bbf3d33870b3fd5e4c77e19c07f8fde2230e7b3d06237e82e29373f7c8a2f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91471273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1287aee122920357f487f9a6570138198110312049bd295f104226783618d190`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:17:30 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:17:30 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 12 Mar 2024 02:17:30 GMT
ENV EMQX_VERSION=5.2.1
# Tue, 12 Mar 2024 02:17:31 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Tue, 12 Mar 2024 02:17:31 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Tue, 12 Mar 2024 02:17:31 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 12 Mar 2024 02:17:39 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Tue, 12 Mar 2024 02:17:40 GMT
WORKDIR /opt/emqx
# Tue, 12 Mar 2024 02:17:40 GMT
USER emqx
# Tue, 12 Mar 2024 02:17:40 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 12 Mar 2024 02:17:40 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 12 Mar 2024 02:17:40 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 12 Mar 2024 02:17:40 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 02:17:40 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007e069718125e27b2758a0a96ce61f99a6cd8e2ca503169bd4462afd919323a`  
		Last Modified: Tue, 12 Mar 2024 02:18:53 GMT  
		Size: 1.6 MB (1644126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab74df7146544658a70ea7f340fb296449ff02f8effc4328e9ef4b73eac0cf5`  
		Last Modified: Tue, 12 Mar 2024 02:18:52 GMT  
		Size: 4.1 KB (4114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f11560836f8b46ac6904429b51a75753f80984355ffdba1e432c1fb46aeb471`  
		Last Modified: Tue, 12 Mar 2024 02:18:57 GMT  
		Size: 59.8 MB (59751015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cf4b35331a0aad71e1b5d388f5df6be66a567c7ce1af6009fd06176431ceea`  
		Last Modified: Tue, 12 Mar 2024 02:18:52 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.2.1`

```console
$ docker pull emqx@sha256:4f0602463b4ba3183639e513744d8f9c1b71722c001d0946301ffb6739c48bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.2.1` - linux; amd64

```console
$ docker pull emqx@sha256:c7842d4a63d6f2ac6d385f714f382c5ee2a63b4454840674814a6abda6bfc4cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101172431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02cf8be8d7d1856c4cb09c41522e9d94fa6f4da7038b735cd19a94c251a09748`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:09:41 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:09:42 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 10 Apr 2024 07:09:42 GMT
ENV EMQX_VERSION=5.2.1
# Wed, 10 Apr 2024 07:09:42 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Wed, 10 Apr 2024 07:09:42 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Wed, 10 Apr 2024 07:09:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 07:09:53 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Wed, 10 Apr 2024 07:09:54 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 07:09:54 GMT
USER emqx
# Wed, 10 Apr 2024 07:09:54 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 07:09:54 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 07:09:54 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 10 Apr 2024 07:09:54 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 07:09:54 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659bee472f61e6a5c34eeeeb6b52574444c8f0f00fee74a8d7647be4feec6332`  
		Last Modified: Wed, 10 Apr 2024 07:11:47 GMT  
		Size: 1.6 MB (1629581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e3164039a5500ecd1b07faccf899e4c31871251f9733ec1948fc78fe32e305`  
		Last Modified: Wed, 10 Apr 2024 07:11:46 GMT  
		Size: 4.1 KB (4100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0db93238eabe5784aacd12eb497a576d4b67a8f47b2b042c2e8157f463086d6`  
		Last Modified: Wed, 10 Apr 2024 07:11:53 GMT  
		Size: 68.1 MB (68110109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a22bc1c301f31f63c12ddb59c936825db2a363474fbad4e8a497997d838905`  
		Last Modified: Wed, 10 Apr 2024 07:11:46 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.2.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:398bbf3d33870b3fd5e4c77e19c07f8fde2230e7b3d06237e82e29373f7c8a2f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91471273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1287aee122920357f487f9a6570138198110312049bd295f104226783618d190`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:17:30 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:17:30 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 12 Mar 2024 02:17:30 GMT
ENV EMQX_VERSION=5.2.1
# Tue, 12 Mar 2024 02:17:31 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Tue, 12 Mar 2024 02:17:31 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Tue, 12 Mar 2024 02:17:31 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 12 Mar 2024 02:17:39 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Tue, 12 Mar 2024 02:17:40 GMT
WORKDIR /opt/emqx
# Tue, 12 Mar 2024 02:17:40 GMT
USER emqx
# Tue, 12 Mar 2024 02:17:40 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 12 Mar 2024 02:17:40 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 12 Mar 2024 02:17:40 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 12 Mar 2024 02:17:40 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 02:17:40 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007e069718125e27b2758a0a96ce61f99a6cd8e2ca503169bd4462afd919323a`  
		Last Modified: Tue, 12 Mar 2024 02:18:53 GMT  
		Size: 1.6 MB (1644126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab74df7146544658a70ea7f340fb296449ff02f8effc4328e9ef4b73eac0cf5`  
		Last Modified: Tue, 12 Mar 2024 02:18:52 GMT  
		Size: 4.1 KB (4114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f11560836f8b46ac6904429b51a75753f80984355ffdba1e432c1fb46aeb471`  
		Last Modified: Tue, 12 Mar 2024 02:18:57 GMT  
		Size: 59.8 MB (59751015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cf4b35331a0aad71e1b5d388f5df6be66a567c7ce1af6009fd06176431ceea`  
		Last Modified: Tue, 12 Mar 2024 02:18:52 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.3`

```console
$ docker pull emqx@sha256:ccad70b36673a4c8e5b7dc1d6ed313e18f05ceaaa192388ebc7c696e539950d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.3` - linux; amd64

```console
$ docker pull emqx@sha256:e5f1af09cac9d50e42fd97cc2e93ee9f9cc118f09803a4f5fd74827ed2362a31
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101788561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:600c659e067ff96b2bff11f1c964d80e643f7a88dc65b322fb7c8c4147823fc1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:09:57 GMT
ENV EMQX_VERSION=5.3.2
# Wed, 10 Apr 2024 07:09:57 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Wed, 10 Apr 2024 07:09:57 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Wed, 10 Apr 2024 07:09:57 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 07:10:11 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:10:11 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 07:10:11 GMT
USER emqx
# Wed, 10 Apr 2024 07:10:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 07:10:12 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 07:10:12 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 10 Apr 2024 07:10:12 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 07:10:12 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a97575f9a741c04405eaf409f32f3383756408e452b1f8254eadfa1818cbe5`  
		Last Modified: Wed, 10 Apr 2024 07:12:09 GMT  
		Size: 70.4 MB (70359921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db5db75a5d47b30115b1cea0d499181edd6019befbfdec1c5d74f93f80e273b`  
		Last Modified: Wed, 10 Apr 2024 07:12:01 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.3` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:31dabf0113b10ffdcdb086b244010e5f3e03d16fb158ca9440a4c1ddc020ae26
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92085829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd7af769fb4ab0ad5c1d282d924618a80aa83a175d3488784ab31ee843b6c27`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:17:42 GMT
ENV EMQX_VERSION=5.3.2
# Tue, 12 Mar 2024 02:17:42 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Tue, 12 Mar 2024 02:17:43 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Tue, 12 Mar 2024 02:17:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 12 Mar 2024 02:17:53 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:17:54 GMT
WORKDIR /opt/emqx
# Tue, 12 Mar 2024 02:17:54 GMT
USER emqx
# Tue, 12 Mar 2024 02:17:54 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 12 Mar 2024 02:17:54 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 12 Mar 2024 02:17:54 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 12 Mar 2024 02:17:54 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 02:17:54 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d507d8d999b67e3706a3998a931e8df2b4e659c45e84f8132fde441afb5d9b4b`  
		Last Modified: Tue, 12 Mar 2024 02:19:11 GMT  
		Size: 62.0 MB (62013812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ba97da2fe61af521c7c0fcdcd1b5ebdf21f3b3b254183b41920c86a71bfe43`  
		Last Modified: Tue, 12 Mar 2024 02:19:05 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.3.2`

```console
$ docker pull emqx@sha256:ccad70b36673a4c8e5b7dc1d6ed313e18f05ceaaa192388ebc7c696e539950d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.3.2` - linux; amd64

```console
$ docker pull emqx@sha256:e5f1af09cac9d50e42fd97cc2e93ee9f9cc118f09803a4f5fd74827ed2362a31
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101788561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:600c659e067ff96b2bff11f1c964d80e643f7a88dc65b322fb7c8c4147823fc1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:09:57 GMT
ENV EMQX_VERSION=5.3.2
# Wed, 10 Apr 2024 07:09:57 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Wed, 10 Apr 2024 07:09:57 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Wed, 10 Apr 2024 07:09:57 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 07:10:11 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:10:11 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 07:10:11 GMT
USER emqx
# Wed, 10 Apr 2024 07:10:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 07:10:12 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 07:10:12 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 10 Apr 2024 07:10:12 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 07:10:12 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a97575f9a741c04405eaf409f32f3383756408e452b1f8254eadfa1818cbe5`  
		Last Modified: Wed, 10 Apr 2024 07:12:09 GMT  
		Size: 70.4 MB (70359921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db5db75a5d47b30115b1cea0d499181edd6019befbfdec1c5d74f93f80e273b`  
		Last Modified: Wed, 10 Apr 2024 07:12:01 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.3.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:31dabf0113b10ffdcdb086b244010e5f3e03d16fb158ca9440a4c1ddc020ae26
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92085829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd7af769fb4ab0ad5c1d282d924618a80aa83a175d3488784ab31ee843b6c27`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:17:42 GMT
ENV EMQX_VERSION=5.3.2
# Tue, 12 Mar 2024 02:17:42 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Tue, 12 Mar 2024 02:17:43 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Tue, 12 Mar 2024 02:17:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 12 Mar 2024 02:17:53 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:17:54 GMT
WORKDIR /opt/emqx
# Tue, 12 Mar 2024 02:17:54 GMT
USER emqx
# Tue, 12 Mar 2024 02:17:54 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 12 Mar 2024 02:17:54 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 12 Mar 2024 02:17:54 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 12 Mar 2024 02:17:54 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 02:17:54 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d507d8d999b67e3706a3998a931e8df2b4e659c45e84f8132fde441afb5d9b4b`  
		Last Modified: Tue, 12 Mar 2024 02:19:11 GMT  
		Size: 62.0 MB (62013812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ba97da2fe61af521c7c0fcdcd1b5ebdf21f3b3b254183b41920c86a71bfe43`  
		Last Modified: Tue, 12 Mar 2024 02:19:05 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.4`

```console
$ docker pull emqx@sha256:141c449e16d9a517226d1efa7b699ed18bc95a21dd5c1e196f0158828cc63049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.4` - linux; amd64

```console
$ docker pull emqx@sha256:b0d4142d8610b259f3d06044083bc2e42fabb6ea4d122b35807508d44fb0c2ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118703418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815f4b8e2c23d2099c7132ced8342732b6e7d8354c9abea90f7f37526cad2176`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:10:18 GMT
ENV EMQX_VERSION=5.4.1
# Wed, 10 Apr 2024 07:10:18 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Wed, 10 Apr 2024 07:10:18 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Wed, 10 Apr 2024 07:10:18 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 07:10:33 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:10:33 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 07:10:34 GMT
USER emqx
# Wed, 10 Apr 2024 07:10:34 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 07:10:34 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 07:10:34 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 10 Apr 2024 07:10:34 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 07:10:34 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00106a8a1247286972b6d5b4b36692ee17ea2d97c5f334ec7736971208573f8`  
		Last Modified: Wed, 10 Apr 2024 07:12:26 GMT  
		Size: 87.3 MB (87274778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be8c9fc1c2ef13a842fbf6aff2874b9fbc105340b9a6b7eb9d61754fc7fa714`  
		Last Modified: Wed, 10 Apr 2024 07:12:17 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:406d2f762d702345233baa09527fa4cb16fc38514e1704d5bbd0982f171494a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108481354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b702434caf6e8f7c9e7394346117e87d0dfba37ad9ffe545ea9ec29c12a21f0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:17:56 GMT
ENV EMQX_VERSION=5.4.1
# Tue, 12 Mar 2024 02:17:56 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Tue, 12 Mar 2024 02:17:56 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Tue, 12 Mar 2024 02:17:56 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 12 Mar 2024 02:18:08 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:18:09 GMT
WORKDIR /opt/emqx
# Tue, 12 Mar 2024 02:18:09 GMT
USER emqx
# Tue, 12 Mar 2024 02:18:09 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 12 Mar 2024 02:18:09 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 12 Mar 2024 02:18:09 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 12 Mar 2024 02:18:09 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 02:18:09 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cd1c48a9c9547261516981126f8f085bc01c935c29d9f09722edd40ade60fa`  
		Last Modified: Tue, 12 Mar 2024 02:19:26 GMT  
		Size: 78.4 MB (78409337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7af450392d45a0ba0b181eb6ac29cb43ce2d0aaa5b7284045806e4ad27b5bd3`  
		Last Modified: Tue, 12 Mar 2024 02:19:19 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.4.1`

```console
$ docker pull emqx@sha256:141c449e16d9a517226d1efa7b699ed18bc95a21dd5c1e196f0158828cc63049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.4.1` - linux; amd64

```console
$ docker pull emqx@sha256:b0d4142d8610b259f3d06044083bc2e42fabb6ea4d122b35807508d44fb0c2ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118703418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815f4b8e2c23d2099c7132ced8342732b6e7d8354c9abea90f7f37526cad2176`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:10:18 GMT
ENV EMQX_VERSION=5.4.1
# Wed, 10 Apr 2024 07:10:18 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Wed, 10 Apr 2024 07:10:18 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Wed, 10 Apr 2024 07:10:18 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 07:10:33 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:10:33 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 07:10:34 GMT
USER emqx
# Wed, 10 Apr 2024 07:10:34 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 07:10:34 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 07:10:34 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 10 Apr 2024 07:10:34 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 07:10:34 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00106a8a1247286972b6d5b4b36692ee17ea2d97c5f334ec7736971208573f8`  
		Last Modified: Wed, 10 Apr 2024 07:12:26 GMT  
		Size: 87.3 MB (87274778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be8c9fc1c2ef13a842fbf6aff2874b9fbc105340b9a6b7eb9d61754fc7fa714`  
		Last Modified: Wed, 10 Apr 2024 07:12:17 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.4.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:406d2f762d702345233baa09527fa4cb16fc38514e1704d5bbd0982f171494a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108481354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b702434caf6e8f7c9e7394346117e87d0dfba37ad9ffe545ea9ec29c12a21f0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:17:56 GMT
ENV EMQX_VERSION=5.4.1
# Tue, 12 Mar 2024 02:17:56 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Tue, 12 Mar 2024 02:17:56 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Tue, 12 Mar 2024 02:17:56 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 12 Mar 2024 02:18:08 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:18:09 GMT
WORKDIR /opt/emqx
# Tue, 12 Mar 2024 02:18:09 GMT
USER emqx
# Tue, 12 Mar 2024 02:18:09 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 12 Mar 2024 02:18:09 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 12 Mar 2024 02:18:09 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 12 Mar 2024 02:18:09 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 02:18:09 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cd1c48a9c9547261516981126f8f085bc01c935c29d9f09722edd40ade60fa`  
		Last Modified: Tue, 12 Mar 2024 02:19:26 GMT  
		Size: 78.4 MB (78409337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7af450392d45a0ba0b181eb6ac29cb43ce2d0aaa5b7284045806e4ad27b5bd3`  
		Last Modified: Tue, 12 Mar 2024 02:19:19 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.5`

```console
$ docker pull emqx@sha256:82ca993480857e600c8452dd4c5fcf8cd6e770d475621834ca3d0bd1721ae15d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.5` - linux; amd64

```console
$ docker pull emqx@sha256:5efce21eced38b8faa9e37088511728d05e4065b5e279d096a1b61edaebdc68b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121268493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac34f32f6c6596b90f03a6eec508c1fbde04f7171e60d1c7e60583e92b20cd77`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:10:38 GMT
ENV EMQX_VERSION=5.5.1
# Wed, 10 Apr 2024 07:10:38 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Wed, 10 Apr 2024 07:10:38 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Wed, 10 Apr 2024 07:10:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 07:10:54 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 10 Apr 2024 07:10:54 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 07:10:54 GMT
USER emqx
# Wed, 10 Apr 2024 07:10:54 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 07:10:55 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 07:10:55 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Wed, 10 Apr 2024 07:10:55 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 07:10:55 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135438a2d2de091ce5a0d87c8afd5a17e05038759ea9d60b1dc2464757c901fd`  
		Last Modified: Wed, 10 Apr 2024 07:12:44 GMT  
		Size: 89.8 MB (89839721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94547f34bc606d0b03a2f12b19f212f9195a4ef5b3ebf35f87fc966b849bfaa`  
		Last Modified: Wed, 10 Apr 2024 07:12:34 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:6e6d51bccd322aa25174396f668bca9bea4d199da65ac09030007d0e05a4161b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116779356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06075f13a7201d9274873b0cc4542f762daca156e1af78d8d74e604206024c89`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:18:12 GMT
ENV EMQX_VERSION=5.5.1
# Tue, 12 Mar 2024 02:18:13 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Tue, 12 Mar 2024 02:18:13 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Tue, 12 Mar 2024 02:18:13 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 04 Apr 2024 20:05:04 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 04 Apr 2024 20:05:05 GMT
WORKDIR /opt/emqx
# Thu, 04 Apr 2024 20:05:05 GMT
USER emqx
# Thu, 04 Apr 2024 20:05:05 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 04 Apr 2024 20:05:05 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 04 Apr 2024 20:05:05 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Thu, 04 Apr 2024 20:05:05 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 04 Apr 2024 20:05:06 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342b4be32f1ed9ad08302312bdcb9b35ba2a9ba0cd84c02620cca524069a64f0`  
		Last Modified: Thu, 04 Apr 2024 20:05:57 GMT  
		Size: 86.7 MB (86707204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec66b18f48f972245acd08b8bf1c1bc9862659edac00d5e9ec69f4584a40ce5`  
		Last Modified: Thu, 04 Apr 2024 20:05:50 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.5.1`

```console
$ docker pull emqx@sha256:82ca993480857e600c8452dd4c5fcf8cd6e770d475621834ca3d0bd1721ae15d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.5.1` - linux; amd64

```console
$ docker pull emqx@sha256:5efce21eced38b8faa9e37088511728d05e4065b5e279d096a1b61edaebdc68b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121268493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac34f32f6c6596b90f03a6eec508c1fbde04f7171e60d1c7e60583e92b20cd77`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:10:38 GMT
ENV EMQX_VERSION=5.5.1
# Wed, 10 Apr 2024 07:10:38 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Wed, 10 Apr 2024 07:10:38 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Wed, 10 Apr 2024 07:10:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 07:10:54 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 10 Apr 2024 07:10:54 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 07:10:54 GMT
USER emqx
# Wed, 10 Apr 2024 07:10:54 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 07:10:55 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 07:10:55 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Wed, 10 Apr 2024 07:10:55 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 07:10:55 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135438a2d2de091ce5a0d87c8afd5a17e05038759ea9d60b1dc2464757c901fd`  
		Last Modified: Wed, 10 Apr 2024 07:12:44 GMT  
		Size: 89.8 MB (89839721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94547f34bc606d0b03a2f12b19f212f9195a4ef5b3ebf35f87fc966b849bfaa`  
		Last Modified: Wed, 10 Apr 2024 07:12:34 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.5.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:6e6d51bccd322aa25174396f668bca9bea4d199da65ac09030007d0e05a4161b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116779356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06075f13a7201d9274873b0cc4542f762daca156e1af78d8d74e604206024c89`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:18:12 GMT
ENV EMQX_VERSION=5.5.1
# Tue, 12 Mar 2024 02:18:13 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Tue, 12 Mar 2024 02:18:13 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Tue, 12 Mar 2024 02:18:13 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 04 Apr 2024 20:05:04 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 04 Apr 2024 20:05:05 GMT
WORKDIR /opt/emqx
# Thu, 04 Apr 2024 20:05:05 GMT
USER emqx
# Thu, 04 Apr 2024 20:05:05 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 04 Apr 2024 20:05:05 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 04 Apr 2024 20:05:05 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Thu, 04 Apr 2024 20:05:05 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 04 Apr 2024 20:05:06 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342b4be32f1ed9ad08302312bdcb9b35ba2a9ba0cd84c02620cca524069a64f0`  
		Last Modified: Thu, 04 Apr 2024 20:05:57 GMT  
		Size: 86.7 MB (86707204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec66b18f48f972245acd08b8bf1c1bc9862659edac00d5e9ec69f4584a40ce5`  
		Last Modified: Thu, 04 Apr 2024 20:05:50 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.6`

```console
$ docker pull emqx@sha256:eeb7d4644febb2653ebc0e8af835f5022012e46e912af42e4259914734c15a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.6` - linux; amd64

```console
$ docker pull emqx@sha256:2842db71854f230d76883f41a4c85e00164909c29a40cfc52947cfe2ebad2a0c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (121967256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e156bccc4eee382f32c9b0db5ccd573f2490d83968c4fff7277d6d675f5b1de4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:10:59 GMT
ENV EMQX_VERSION=5.6.0
# Wed, 10 Apr 2024 07:10:59 GMT
ENV AMD64_SHA256=d04535234c91dada9ae794247ccc70139c980c24a2f4609e8253c95e75b992ec
# Wed, 10 Apr 2024 07:10:59 GMT
ENV ARM64_SHA256=c40a6f7a70fce3874a4db804cb908f808a0119d77d1db324bdf3050b7429f31d
# Wed, 10 Apr 2024 07:10:59 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 07:11:16 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     apt-get clean;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 10 Apr 2024 07:11:16 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 07:11:16 GMT
USER emqx
# Wed, 10 Apr 2024 07:11:16 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 07:11:16 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 07:11:17 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Wed, 10 Apr 2024 07:11:17 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 07:11:17 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97bd7388580f03db39cddd67403c46b04e503642fb9c7c08290acf9e397edd5`  
		Last Modified: Wed, 10 Apr 2024 07:13:01 GMT  
		Size: 92.8 MB (92834864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2e141b774b38a6b8c7b8afd956fc6432a04b878c2a483b4c378d605bd38dd5`  
		Last Modified: Wed, 10 Apr 2024 07:12:52 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.6` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:f5738e10c2c3ed991760301957d2405565903fa29b7610796e1c9e229a2a4e1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.6 MB (118551298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43892ef99d6270cdd081b4916b189c2ae090cdcef53ad86b37a597e69e40acd`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Thu, 04 Apr 2024 20:05:11 GMT
ENV EMQX_VERSION=5.6.0
# Thu, 04 Apr 2024 20:05:11 GMT
ENV AMD64_SHA256=d04535234c91dada9ae794247ccc70139c980c24a2f4609e8253c95e75b992ec
# Thu, 04 Apr 2024 20:05:11 GMT
ENV ARM64_SHA256=c40a6f7a70fce3874a4db804cb908f808a0119d77d1db324bdf3050b7429f31d
# Thu, 04 Apr 2024 20:05:11 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 04 Apr 2024 20:05:26 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     apt-get clean;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 04 Apr 2024 20:05:27 GMT
WORKDIR /opt/emqx
# Thu, 04 Apr 2024 20:05:27 GMT
USER emqx
# Thu, 04 Apr 2024 20:05:27 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 04 Apr 2024 20:05:27 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 04 Apr 2024 20:05:27 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Thu, 04 Apr 2024 20:05:27 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 04 Apr 2024 20:05:27 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f35daaece97c1436bc272e916d8f54078b821e6e9c6fa5215c425c72c9def82`  
		Last Modified: Thu, 04 Apr 2024 20:06:13 GMT  
		Size: 89.4 MB (89393828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8171ff5cb00ca906ec69033298157d6f15a528cc1f6450cea2b0f7ab4a73176`  
		Last Modified: Thu, 04 Apr 2024 20:06:05 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.6.0`

```console
$ docker pull emqx@sha256:eeb7d4644febb2653ebc0e8af835f5022012e46e912af42e4259914734c15a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.6.0` - linux; amd64

```console
$ docker pull emqx@sha256:2842db71854f230d76883f41a4c85e00164909c29a40cfc52947cfe2ebad2a0c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (121967256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e156bccc4eee382f32c9b0db5ccd573f2490d83968c4fff7277d6d675f5b1de4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:10:59 GMT
ENV EMQX_VERSION=5.6.0
# Wed, 10 Apr 2024 07:10:59 GMT
ENV AMD64_SHA256=d04535234c91dada9ae794247ccc70139c980c24a2f4609e8253c95e75b992ec
# Wed, 10 Apr 2024 07:10:59 GMT
ENV ARM64_SHA256=c40a6f7a70fce3874a4db804cb908f808a0119d77d1db324bdf3050b7429f31d
# Wed, 10 Apr 2024 07:10:59 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 07:11:16 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     apt-get clean;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 10 Apr 2024 07:11:16 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 07:11:16 GMT
USER emqx
# Wed, 10 Apr 2024 07:11:16 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 07:11:16 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 07:11:17 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Wed, 10 Apr 2024 07:11:17 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 07:11:17 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97bd7388580f03db39cddd67403c46b04e503642fb9c7c08290acf9e397edd5`  
		Last Modified: Wed, 10 Apr 2024 07:13:01 GMT  
		Size: 92.8 MB (92834864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2e141b774b38a6b8c7b8afd956fc6432a04b878c2a483b4c378d605bd38dd5`  
		Last Modified: Wed, 10 Apr 2024 07:12:52 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.6.0` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:f5738e10c2c3ed991760301957d2405565903fa29b7610796e1c9e229a2a4e1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.6 MB (118551298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43892ef99d6270cdd081b4916b189c2ae090cdcef53ad86b37a597e69e40acd`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Thu, 04 Apr 2024 20:05:11 GMT
ENV EMQX_VERSION=5.6.0
# Thu, 04 Apr 2024 20:05:11 GMT
ENV AMD64_SHA256=d04535234c91dada9ae794247ccc70139c980c24a2f4609e8253c95e75b992ec
# Thu, 04 Apr 2024 20:05:11 GMT
ENV ARM64_SHA256=c40a6f7a70fce3874a4db804cb908f808a0119d77d1db324bdf3050b7429f31d
# Thu, 04 Apr 2024 20:05:11 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 04 Apr 2024 20:05:26 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     apt-get clean;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 04 Apr 2024 20:05:27 GMT
WORKDIR /opt/emqx
# Thu, 04 Apr 2024 20:05:27 GMT
USER emqx
# Thu, 04 Apr 2024 20:05:27 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 04 Apr 2024 20:05:27 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 04 Apr 2024 20:05:27 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Thu, 04 Apr 2024 20:05:27 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 04 Apr 2024 20:05:27 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f35daaece97c1436bc272e916d8f54078b821e6e9c6fa5215c425c72c9def82`  
		Last Modified: Thu, 04 Apr 2024 20:06:13 GMT  
		Size: 89.4 MB (89393828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8171ff5cb00ca906ec69033298157d6f15a528cc1f6450cea2b0f7ab4a73176`  
		Last Modified: Thu, 04 Apr 2024 20:06:05 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:eeb7d4644febb2653ebc0e8af835f5022012e46e912af42e4259914734c15a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:2842db71854f230d76883f41a4c85e00164909c29a40cfc52947cfe2ebad2a0c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (121967256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e156bccc4eee382f32c9b0db5ccd573f2490d83968c4fff7277d6d675f5b1de4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:10:59 GMT
ENV EMQX_VERSION=5.6.0
# Wed, 10 Apr 2024 07:10:59 GMT
ENV AMD64_SHA256=d04535234c91dada9ae794247ccc70139c980c24a2f4609e8253c95e75b992ec
# Wed, 10 Apr 2024 07:10:59 GMT
ENV ARM64_SHA256=c40a6f7a70fce3874a4db804cb908f808a0119d77d1db324bdf3050b7429f31d
# Wed, 10 Apr 2024 07:10:59 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 10 Apr 2024 07:11:16 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     apt-get clean;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 10 Apr 2024 07:11:16 GMT
WORKDIR /opt/emqx
# Wed, 10 Apr 2024 07:11:16 GMT
USER emqx
# Wed, 10 Apr 2024 07:11:16 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 10 Apr 2024 07:11:16 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 10 Apr 2024 07:11:17 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Wed, 10 Apr 2024 07:11:17 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 10 Apr 2024 07:11:17 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97bd7388580f03db39cddd67403c46b04e503642fb9c7c08290acf9e397edd5`  
		Last Modified: Wed, 10 Apr 2024 07:13:01 GMT  
		Size: 92.8 MB (92834864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2e141b774b38a6b8c7b8afd956fc6432a04b878c2a483b4c378d605bd38dd5`  
		Last Modified: Wed, 10 Apr 2024 07:12:52 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:f5738e10c2c3ed991760301957d2405565903fa29b7610796e1c9e229a2a4e1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.6 MB (118551298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43892ef99d6270cdd081b4916b189c2ae090cdcef53ad86b37a597e69e40acd`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Thu, 04 Apr 2024 20:05:11 GMT
ENV EMQX_VERSION=5.6.0
# Thu, 04 Apr 2024 20:05:11 GMT
ENV AMD64_SHA256=d04535234c91dada9ae794247ccc70139c980c24a2f4609e8253c95e75b992ec
# Thu, 04 Apr 2024 20:05:11 GMT
ENV ARM64_SHA256=c40a6f7a70fce3874a4db804cb908f808a0119d77d1db324bdf3050b7429f31d
# Thu, 04 Apr 2024 20:05:11 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 04 Apr 2024 20:05:26 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     apt-get clean;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 04 Apr 2024 20:05:27 GMT
WORKDIR /opt/emqx
# Thu, 04 Apr 2024 20:05:27 GMT
USER emqx
# Thu, 04 Apr 2024 20:05:27 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 04 Apr 2024 20:05:27 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 04 Apr 2024 20:05:27 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Thu, 04 Apr 2024 20:05:27 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 04 Apr 2024 20:05:27 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f35daaece97c1436bc272e916d8f54078b821e6e9c6fa5215c425c72c9def82`  
		Last Modified: Thu, 04 Apr 2024 20:06:13 GMT  
		Size: 89.4 MB (89393828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8171ff5cb00ca906ec69033298157d6f15a528cc1f6450cea2b0f7ab4a73176`  
		Last Modified: Thu, 04 Apr 2024 20:06:05 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
