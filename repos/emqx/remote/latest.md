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
