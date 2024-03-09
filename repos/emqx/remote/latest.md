## `emqx:latest`

```console
$ docker pull emqx@sha256:c2b4243fb7d0503b7411aefdf887643d4d918152aa3440f2e1b2177c8a109b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:986417b111b05a9530df6b0321ca4f725ae4d2d08abc45a44396dd47dd60c7f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121263691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1ec485420ee8a94a474647319ead59d8a210bf118c1ce87aa0b352d626849c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Sat, 09 Mar 2024 00:51:21 GMT
ENV EMQX_VERSION=5.5.1
# Sat, 09 Mar 2024 00:51:21 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Sat, 09 Mar 2024 00:51:21 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Sat, 09 Mar 2024 00:51:21 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sat, 09 Mar 2024 00:51:35 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 09 Mar 2024 00:51:35 GMT
WORKDIR /opt/emqx
# Sat, 09 Mar 2024 00:51:35 GMT
USER emqx
# Sat, 09 Mar 2024 00:51:35 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 09 Mar 2024 00:51:35 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Sat, 09 Mar 2024 00:51:36 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Sat, 09 Mar 2024 00:51:36 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 09 Mar 2024 00:51:36 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba48e43b8ff1ebfdbcb605830bf87ff84a8472fd12b6042a5d38b2dbc5e1600`  
		Last Modified: Sat, 09 Mar 2024 00:52:03 GMT  
		Size: 89.8 MB (89840231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31870e450147f7d21ff9bed96f482413360f1faf3be22ab505f006116ada381b`  
		Last Modified: Sat, 09 Mar 2024 00:51:53 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:ba0256d0980d8b8174ed480bab9f74131e879c26064fcc2c9a4ec7085249c26b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116792876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744f4f66f74974181ab2b82f3729b6201e7d720666f1a2c6708526116a8a0a8e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Sat, 09 Mar 2024 01:30:07 GMT
ENV EMQX_VERSION=5.5.1
# Sat, 09 Mar 2024 01:30:07 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Sat, 09 Mar 2024 01:30:07 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Sat, 09 Mar 2024 01:30:07 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sat, 09 Mar 2024 01:30:19 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 09 Mar 2024 01:30:21 GMT
WORKDIR /opt/emqx
# Sat, 09 Mar 2024 01:30:21 GMT
USER emqx
# Sat, 09 Mar 2024 01:30:21 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 09 Mar 2024 01:30:21 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Sat, 09 Mar 2024 01:30:21 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Sat, 09 Mar 2024 01:30:21 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 09 Mar 2024 01:30:21 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be1127cce76560af51b0de23182f7b84157b0d9f351070c7e7af996c141d079d`  
		Last Modified: Sat, 09 Mar 2024 01:30:42 GMT  
		Size: 86.7 MB (86720764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0496fac4217e588e97e67f10da546f918cba1b1597b84536e6d98b5244f567ab`  
		Last Modified: Sat, 09 Mar 2024 01:30:35 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
