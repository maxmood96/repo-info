## `gazebo:libgazebo9-stretch`

```console
$ docker pull gazebo@sha256:6656f4e6ec1d024f62429ca8151abedd3b0ab0b1f1c209e95db37f87379f0bad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo9-stretch` - linux; amd64

```console
$ docker pull gazebo@sha256:6b0e7b8d5b805586c61cd9da481a89239a8bb7b9fb9231d9baad77cbb7f99cc2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **570.2 MB (570173561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d34bb79c0a7de18c9bb4a24c9d5f2b34df03fe4fc9a46e169a9f3f7bf799e1`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Tue, 12 Jan 2021 00:35:05 GMT
ADD file:166cd044a29ad501c753917f07d638932f2ce960a8570b12d9155e8c38d1e917 in / 
# Tue, 12 Jan 2021 00:35:06 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 05:18:25 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 05:18:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Tue, 12 Jan 2021 05:18:31 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Tue, 12 Jan 2021 05:19:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo9=9.16.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 05:19:28 GMT
EXPOSE 11345
# Tue, 12 Jan 2021 05:19:29 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Tue, 12 Jan 2021 05:19:29 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Tue, 12 Jan 2021 05:19:30 GMT
CMD ["gzserver"]
# Tue, 12 Jan 2021 05:21:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo9-dev=9.16.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2587235a7635c6991dfee9791c7977ab29694cf73bc64c3c5a79097ca99364d1`  
		Last Modified: Tue, 12 Jan 2021 00:43:05 GMT  
		Size: 45.4 MB (45380014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9bbdad70e68e511d6d02ff07a87808b7610b3cd8de845ff814b0fbce724166`  
		Last Modified: Tue, 12 Jan 2021 05:22:55 GMT  
		Size: 18.5 MB (18509196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0975e4857e2b7131b970af1dccfc0ce0350d7daafa68ed78e90d3feb402a1e76`  
		Last Modified: Tue, 12 Jan 2021 05:22:49 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:797988657de0005809d9bd994ea471d16805ba3e20d37ee130ae41e81f36844d`  
		Last Modified: Tue, 12 Jan 2021 05:22:49 GMT  
		Size: 5.0 KB (4976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7afb053b5f3f936c95def0641f51578e884782821be8c0f959085b5d89ab2e51`  
		Last Modified: Tue, 12 Jan 2021 05:23:20 GMT  
		Size: 202.3 MB (202271389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:090b031625a3781cedf43ab5b5b6a58af77d153c1cbd0a737403c51feebf1ed6`  
		Last Modified: Tue, 12 Jan 2021 05:22:48 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088708bd6f17ed1f6275736297849e1ef8375ea54a92f3b5020c10f5c163586e`  
		Last Modified: Tue, 12 Jan 2021 05:24:46 GMT  
		Size: 304.0 MB (304006379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
