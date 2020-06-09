## `gazebo:gzserver9-stretch`

```console
$ docker pull gazebo@sha256:eac8b1ad979b74bf3f68f19a4c7700d96346559ffcc45809e1f4a5dda70b240f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver9-stretch` - linux; amd64

```console
$ docker pull gazebo@sha256:a2c942636c8d38b401719c3745f99eed469275b1d2f58e558c7eca8424d95307
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.1 MB (265144136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a41d896f92b765c648764ed2adc80611fa8a6487206b76839d8edc0ddd395457`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:20 GMT
ADD file:6e16bc9cf28c19a1fb1fb516411643e33cbd2bdb7b6c2ce2468c6583c89871a2 in / 
# Tue, 09 Jun 2020 01:23:21 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 06:42:31 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 06:42:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Tue, 09 Jun 2020 06:42:36 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Tue, 09 Jun 2020 06:43:30 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     gazebo9=9.12.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 06:43:31 GMT
EXPOSE 11345
# Tue, 09 Jun 2020 06:43:31 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Tue, 09 Jun 2020 06:43:31 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Tue, 09 Jun 2020 06:43:31 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:81fc1918191541a2ffb6ed1cd8386ef8302aea1b0613ebc768a00e76c1f34bb9`  
		Last Modified: Tue, 09 Jun 2020 01:27:59 GMT  
		Size: 45.4 MB (45375796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c704e84a21229e3d624d57bece432b937a28302cd689d79c84ffce9a8cd5995c`  
		Last Modified: Tue, 09 Jun 2020 06:45:44 GMT  
		Size: 18.5 MB (18500688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae6db3e3b49adef553c9d6346f6c8e8c6fd823ed29583a53b818d236c81a3b4`  
		Last Modified: Tue, 09 Jun 2020 06:45:41 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d127f9a5d11eb78f45c685a8b46d77fbc0dfd93b2ae9f204229b4f94296e62d4`  
		Last Modified: Tue, 09 Jun 2020 06:45:41 GMT  
		Size: 5.0 KB (4974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78cabc80430b964b054924a9674a52bd3f0f8cfa4ad01f8e166cb7a7eb90e55b`  
		Last Modified: Tue, 09 Jun 2020 06:46:12 GMT  
		Size: 201.3 MB (201261070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91fa6e57c0af1ba75b0c64e64a1664abb4ea13848ab2948ad9e3044cc7176fa`  
		Last Modified: Tue, 09 Jun 2020 06:45:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
