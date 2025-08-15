<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.22`](#nats2-alpine322)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-ltsc2022`](#nats2-nanoserver-ltsc2022)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-ltsc2022`](#nats2-windowsservercore-ltsc2022)
-	[`nats:2.10`](#nats210)
-	[`nats:2.10-alpine`](#nats210-alpine)
-	[`nats:2.10-alpine3.22`](#nats210-alpine322)
-	[`nats:2.10-linux`](#nats210-linux)
-	[`nats:2.10-nanoserver`](#nats210-nanoserver)
-	[`nats:2.10-nanoserver-ltsc2022`](#nats210-nanoserver-ltsc2022)
-	[`nats:2.10-scratch`](#nats210-scratch)
-	[`nats:2.10-windowsservercore`](#nats210-windowsservercore)
-	[`nats:2.10-windowsservercore-ltsc2022`](#nats210-windowsservercore-ltsc2022)
-	[`nats:2.10.29`](#nats21029)
-	[`nats:2.10.29-alpine`](#nats21029-alpine)
-	[`nats:2.10.29-alpine3.22`](#nats21029-alpine322)
-	[`nats:2.10.29-linux`](#nats21029-linux)
-	[`nats:2.10.29-nanoserver`](#nats21029-nanoserver)
-	[`nats:2.10.29-nanoserver-ltsc2022`](#nats21029-nanoserver-ltsc2022)
-	[`nats:2.10.29-scratch`](#nats21029-scratch)
-	[`nats:2.10.29-windowsservercore`](#nats21029-windowsservercore)
-	[`nats:2.10.29-windowsservercore-ltsc2022`](#nats21029-windowsservercore-ltsc2022)
-	[`nats:2.11`](#nats211)
-	[`nats:2.11-alpine`](#nats211-alpine)
-	[`nats:2.11-alpine3.22`](#nats211-alpine322)
-	[`nats:2.11-linux`](#nats211-linux)
-	[`nats:2.11-nanoserver`](#nats211-nanoserver)
-	[`nats:2.11-nanoserver-ltsc2022`](#nats211-nanoserver-ltsc2022)
-	[`nats:2.11-scratch`](#nats211-scratch)
-	[`nats:2.11-windowsservercore`](#nats211-windowsservercore)
-	[`nats:2.11-windowsservercore-ltsc2022`](#nats211-windowsservercore-ltsc2022)
-	[`nats:2.11.8`](#nats2118)
-	[`nats:2.11.8-alpine`](#nats2118-alpine)
-	[`nats:2.11.8-alpine3.22`](#nats2118-alpine322)
-	[`nats:2.11.8-linux`](#nats2118-linux)
-	[`nats:2.11.8-nanoserver`](#nats2118-nanoserver)
-	[`nats:2.11.8-nanoserver-ltsc2022`](#nats2118-nanoserver-ltsc2022)
-	[`nats:2.11.8-scratch`](#nats2118-scratch)
-	[`nats:2.11.8-windowsservercore`](#nats2118-windowsservercore)
-	[`nats:2.11.8-windowsservercore-ltsc2022`](#nats2118-windowsservercore-ltsc2022)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.22`](#natsalpine322)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-ltsc2022`](#natsnanoserver-ltsc2022)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-ltsc2022`](#natswindowsservercore-ltsc2022)

## `nats:2`

```console
$ docker pull nats@sha256:86e9fe3e8d887ea2c12322b4231c1f2f64e3c5b9917168198e1ab6c0fe16b222
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.4052; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:5634002bb5af84b0379f0de363bf0027b76bd6cf1a1db66ad254ae945a163cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6340078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d63b90f51c086da0db2adbc1a2ad7102ecabb8fa67c2470fdc2217b40a4d922`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b663fe8cd396789f2474139e39527f819c3a482db5e25e230cacaadd75df18ce`  
		Last Modified: Thu, 14 Aug 2025 17:27:46 GMT  
		Size: 6.3 MB (6339570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e38b65a6463af6a5ebdc0b02115f51a91399b2710a2758586bbeda7b6d50ba`  
		Last Modified: Thu, 14 Aug 2025 17:27:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:2ab05007143b6795815ff8714f15842e070df35013849973ca0b2f3552177ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310bb9bbe1f9febd06c494bb2dd5b961d7bf71acc8bf0b2fb53e0834a8cc2117`

```dockerfile
```

-	Layers:
	-	`sha256:85acdef1c273fe4667fee682e56c38f81137085631f156c2949814b3bc0d0bee`  
		Last Modified: Thu, 14 Aug 2025 20:56:26 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:40d95d59739fe46433103f4d262d1dd789f75ee44e99c640ea6457cf05487501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6054066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492743618ce250d8b5f53bf5f1e12404d57c3ec44625d5b44726e86f9bba5086`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f10f27efc9fb4dc2b4cdaada3f99aa2ffb9ebc99496fd55f1920263e51b914c9`  
		Last Modified: Thu, 14 Aug 2025 18:07:33 GMT  
		Size: 6.1 MB (6053556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bdfede140a8dbbb6956c184b88de98cc1662ecbef253a2a4433bc47021d07dc`  
		Last Modified: Thu, 14 Aug 2025 18:07:33 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:06dde395a53d1e08b8fd585a2037a3d0579d0cf26446b77df720fb5c757064f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b6f621ca40cc0a37945b871d68296b32cdb51732868485359bc907292b6eba`

```dockerfile
```

-	Layers:
	-	`sha256:6cffdd7549f5659166afe24fb85e23cfebf2409e108e1f347151569e8e28ba38`  
		Last Modified: Thu, 14 Aug 2025 20:56:30 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:815e928020aef447482878a6cef15fd72ac0f9d767b8309b032f7fb8feb7a353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6043424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbbf5945fb4360c4f621c54027b1cb47034cc2fa4d455ccc3f90923c1fe13761`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ba52e77e96ac90555714325e16a7b63d377c42dbeec68ba24cd503063cf7b9e0`  
		Last Modified: Thu, 14 Aug 2025 17:27:10 GMT  
		Size: 6.0 MB (6042914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ee5e05524b58d5802a62546f6f2347446d5321c4e8d583722db5b777d831d1`  
		Last Modified: Thu, 14 Aug 2025 17:27:08 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:842f4f4569460f34fc562978f687fc36581c388b02ab14cdad623893d588f5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2b1c717567f7faa2dde66fcb89acd6dcf382ec81408e1c26ecb2d68f03d105`

```dockerfile
```

-	Layers:
	-	`sha256:62da1307e4b0132c952bdd53d1b82eb3e96fa2934b1b582a8b7277351ddc31cd`  
		Last Modified: Thu, 14 Aug 2025 20:56:33 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d46af1d33927787659e676ea4714a6d53c8ba71956e0cda595d30ab277af5341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b7bb1d1d30e4a8233087664e0b5540f3e42f49f27589cfb43d23bacbeb63ffe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5823b59d47a0c660012e09655022b6660ce21c617ee2978f3edacb2ac344cb9f`  
		Last Modified: Thu, 14 Aug 2025 19:46:02 GMT  
		Size: 5.8 MB (5827281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e915dc222e2df5e58849a12f73e5fcede2bc08f2c98fd12f234ad34883849b`  
		Last Modified: Thu, 14 Aug 2025 19:46:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:4e9ff58758ddaea565568a15d4d049d69f51f01f69e9e0e517c68718dfe93ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a92dc3160475131a9aa4330ac0e14dedb97f5d4d57d5a386b4b1033afe203bc`

```dockerfile
```

-	Layers:
	-	`sha256:efd6b414c46e44a7c6cd8407e5887b4066f7e91785d16647bdfc24cb7dfb35a4`  
		Last Modified: Thu, 14 Aug 2025 20:56:36 GMT  
		Size: 10.6 KB (10649 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; ppc64le

```console
$ docker pull nats@sha256:70ad109d17470e9dbefe10df2ea372ea487e5a28cf96934110c5f6e6b118c4ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5807845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcf49d098aee252cf17a17945623b98c12312f01460230bd2494a20949c2703`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:221614c6b4427295323da315f973992219d61abd51aa73f549b80d617ceed783`  
		Last Modified: Thu, 14 Aug 2025 20:45:44 GMT  
		Size: 5.8 MB (5807337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea070ca5e9aa9e1edaa1764d931a0b0e385793e5b3124004b4ba91da5efc9e9`  
		Last Modified: Thu, 14 Aug 2025 20:45:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:bf4cec841a590e736bc48410cd41b4eb5176b07e39b161d5827a0dfe411fb72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd14ce8eff83929fceb915b93bd248d9837b402d7c289ab095bb35b5306608d`

```dockerfile
```

-	Layers:
	-	`sha256:f968b5bb7ad9cd95b31e5948c6d247e8ff2820fa830ca084746ac40f662b15d1`  
		Last Modified: Thu, 14 Aug 2025 23:56:26 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - linux; s390x

```console
$ docker pull nats@sha256:66e24c97e22fd4db570efbde5c154dad761a934509688d1066ff6faf16c6ff8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6173621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5239fb0f4852c75ada10240d6ad54ccabbe1c300c54385271ab0d9c9a16d599`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 Aug 2025 12:51:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 Aug 2025 12:51:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 Aug 2025 12:51:02 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 Aug 2025 12:51:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 Aug 2025 12:51:02 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 Aug 2025 12:51:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:84a200250dfb971cfcf23197670e7ccfcfae55787bc8842c737081462376b978`  
		Last Modified: Mon, 04 Aug 2025 18:10:15 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5013d749e0797d9a012b7f969383e42b359cae57b7b1945f62eae07e6f12bbb`  
		Last Modified: Mon, 04 Aug 2025 18:10:15 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2` - unknown; unknown

```console
$ docker pull nats@sha256:3e90c2e5acc844d0189d6d664df76b3fc55d6438e1be7c1146763d00098ed8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469d8c0a969e19358745ad9513225279dd13b3d004003729b94ccd524773ffb5`

```dockerfile
```

-	Layers:
	-	`sha256:3490df75b7ac2f5425cf2a5decc578d60f595e9e0317faa4e73c20548b16f138`  
		Last Modified: Mon, 04 Aug 2025 20:56:51 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:ad9de8f09f3634777b25adb56728db4ae6804eb3e93cf167d338af2569150272
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129178975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3e567374bac2065f94b8560a0f1747b427e881b5faa654919d1f7abccc554d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Thu, 14 Aug 2025 18:14:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 14 Aug 2025 18:14:05 GMT
RUN cmd /S /C #(nop) COPY file:3fa3039439cf4074860757aeaaa6c458fcb2a8fd53320637e2edb93570462bde in C:\nats-server.exe 
# Thu, 14 Aug 2025 18:14:06 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Aug 2025 18:14:07 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 14 Aug 2025 18:14:08 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Aug 2025 18:14:09 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70dd762bbc2519848d92e4250ffd2e8ad506e67e2ccc6edb8b28deb7bd6a4cc3`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8303cc1b67f588378cd15d48f0f9092ea5f9e1d8e2832d99a509bdd9c8ff70a`  
		Last Modified: Thu, 14 Aug 2025 18:14:54 GMT  
		Size: 6.5 MB (6512850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5204fc3573607851e777581d8f3393c06877a1b385138e9ddb562e41c44ae04f`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5811e67cadd8e8c18aa9f537c4147610482318cb56ca5e6a1ff3cff5d96e4cfc`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b880e68edcdaf39200bd33cc61fd60fab56c1eae85a872652a20730da3d12a`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbef80910535149a3762e6bfc014c51084a8c11fa366889b246185411c39fb9`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:71092f77d707a4a81b12aca5096d6b2d2e07ad16aa57c84066940a17af74f61a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:9e5633ac7584fc4e80d34be3ff7e15aa3fabec79a5573c2d9abefcf1f7761d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10586751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dfa54630538e8565a0953e5d7316c4b92bd17e293ec333e94f52be2094e7300`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ab6e8880f219a2dd7752796195d9939c137da1ea12c10015c60812ca497573`  
		Last Modified: Thu, 14 Aug 2025 17:21:49 GMT  
		Size: 6.8 MB (6786090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283833608b5ae7ddb376c701f296ad922908c7627de5632ba6e83601e7ac8355`  
		Last Modified: Thu, 14 Aug 2025 17:21:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3411c495c894b3b46ad114eceb39fb6deff204dacab199804c51fd2e1a33a5ae`  
		Last Modified: Thu, 14 Aug 2025 17:21:49 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d90e427f49684d9b241e599c42a542365675aa62dd6d92a617694d503903cfcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299652c57abf36d15568386e529c8a81ada9d5600ced03a88bccc20b7a50be31`

```dockerfile
```

-	Layers:
	-	`sha256:4ff271d6ce9dacd8101fce3d16eda36e2bbe12422efe9c37df07a8f681004669`  
		Last Modified: Thu, 14 Aug 2025 17:56:25 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:2cfaa354cfe1d863108af5b170d266f632b75f3785be68158e9e0cd1170c640a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10004611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:decbc388e2e168ea436dfa71f5e8cac800997860eb2b021cab4f5e4eec76027f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381ebd5419e3fec8229c2bc4e50847a161b2d4865cfcb4e6733a0ea3c32c77b4`  
		Last Modified: Thu, 14 Aug 2025 18:30:15 GMT  
		Size: 6.5 MB (6502730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37fce2ec2d65289a1c9ac7f39b6ae87b35135e3b107484e7e844793f8d7ff565`  
		Last Modified: Thu, 14 Aug 2025 17:37:15 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872252a349b6a653af65ab2ffc9f0d3cf5eeca6d0e42153f5c303d068d5e1812`  
		Last Modified: Thu, 14 Aug 2025 17:37:18 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:14ef749c437d808301a1efe45e399507ff98890b94c616d0007f1534cc8ab482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac20fd9b620208d75d0fd87edc4b9f19c291e788b7e21cc16cbdb65e53dac741`

```dockerfile
```

-	Layers:
	-	`sha256:57504cb714044ba92951c29c12ec66ede4547725749d0a068268c4cb751a035d`  
		Last Modified: Thu, 14 Aug 2025 20:56:44 GMT  
		Size: 14.8 KB (14821 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:1dc6b44e4b33dbe327dda601fff6bb363ef44c34a4ab2177f307f2d9937f49a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9712521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8885fe376c67ec4357739c5950356acebf63efd04e908fdd24e82f77fbfc7511`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b47ccb42d9de5fae140120c5d63f9ac56f0c1a50c858bfdb2926a8b8c9fa01`  
		Last Modified: Thu, 14 Aug 2025 17:20:49 GMT  
		Size: 6.5 MB (6492514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ae165d2cd161f3b90c15a6ebf63ef30cd24b1314b6c1c9ccfdfe1929e38949`  
		Last Modified: Thu, 14 Aug 2025 17:20:49 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0ad244a682bc355346daaf39628ff905c5a9830e058a1e989c513f9abf0f34`  
		Last Modified: Thu, 14 Aug 2025 17:20:49 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f63e9df6411bb2032dedb0fe108e98c278fa2dc1239ac4181f3aefe3dc522497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e855d196a62bbe9f94bd2c44e04b0d5cacb3afdcd63e28f775fa65001122f6a0`

```dockerfile
```

-	Layers:
	-	`sha256:d69e84adacba24383fb74725a58e3be312fd8246fa5942fd3aa8c1b8b60cc567`  
		Last Modified: Thu, 14 Aug 2025 17:56:31 GMT  
		Size: 14.8 KB (14821 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e2578c673d8e347750aad6968df9283d0902cf83b36f7f52eaa2c169fde4886c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10409365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21abd46018664ec1d774ed0ccf028420f6687e33f812018fc3a910dc1ce6014`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdc9114678c7494cfff4d6d27e8c14856724b7b46c06d21e6f5309bb10cfd3e`  
		Last Modified: Thu, 14 Aug 2025 18:48:38 GMT  
		Size: 6.3 MB (6277644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9345987e164f0a7a3c9724b12596354d6f5b27a55c274c5943cf749ce9826044`  
		Last Modified: Thu, 14 Aug 2025 18:48:37 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac90761c84b8f60ad18110b9e9ff4b720ab1d809ff03b57faf042e634d59447`  
		Last Modified: Thu, 14 Aug 2025 18:48:38 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5b917f85bbda7141f8205a4c9d33e28145986c0124ea61f249bd1dbddc4eb538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b21a2426a39cfaf66ebf67d14f2866bfd16bf48c2083eed033b2421bd386a90`

```dockerfile
```

-	Layers:
	-	`sha256:e7738d4b72278c061ab6dd0a6f25f99f4c87e2797157b8dac4f79cea46c6760a`  
		Last Modified: Thu, 14 Aug 2025 20:56:49 GMT  
		Size: 14.9 KB (14865 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:30ad03d77dfb5de88442d0f29c490713d82448efd77693faf7b0935a99453b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9985901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23f66326a77590bc41eb0a5f9f97a5c40ca317276be7cdaf7f7322df7416182`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3e45745642d3a22ccb49be50acc20c0214bd2a5273c0975019b6597df4b5d2`  
		Last Modified: Thu, 14 Aug 2025 18:56:45 GMT  
		Size: 6.3 MB (6257816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a20674adfb2e91f75f547789596c957e2840dfa110ac58dcec2f5e6b686fcd`  
		Last Modified: Thu, 14 Aug 2025 18:56:43 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f76e967ee5d9ae2c5527cef9bb9c8edd4f553ba6495330dc86ee3565f14fc6`  
		Last Modified: Thu, 14 Aug 2025 18:56:43 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:050addcc71308640a4197a465ab8b25fd37500d546c2fbade4232636badd6976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44be2d0d1465d7c59fd92abeb1e0ea0dc33b19b0122cfa12d0204c30e4d4ae13`

```dockerfile
```

-	Layers:
	-	`sha256:66f52a56e2b84f4136709b50caf6b3e34917205c3aeba573456e28d55213cdaa`  
		Last Modified: Thu, 14 Aug 2025 20:56:52 GMT  
		Size: 14.8 KB (14781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:2bf7f126291a09aa21ef2c65fc041fedfe9e9e29e16a8858bf193280e1318fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10271313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e03788a43a2cfeaefbb6d84b08849b6b847b39eeab7af6cfa746c5475cc49a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813401984db76a6756e0db9016fe48ee5c9d82865d147dd243a26b51b2aad684`  
		Last Modified: Thu, 14 Aug 2025 18:35:37 GMT  
		Size: 6.6 MB (6625370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968c785997911db8d7fa72cfc92186b2fc98d2dd5485d575df8bede6c19e3837`  
		Last Modified: Thu, 14 Aug 2025 18:35:38 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5213bbb60ea3349a52da162a1ed048b3650fabc2973bb84980b33601e46410af`  
		Last Modified: Thu, 14 Aug 2025 18:35:37 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:068c939c8d89bfd8a734c0c4fcb03e2f6122fb7cb278e2af5857d850feb3c05c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f0a7a9a995483ed6030887daaf0da034c453fa869bd81b7cb6c7e352c4e8daa`

```dockerfile
```

-	Layers:
	-	`sha256:4f8fbf204f658abfd1d495febd491047b4ab613c794be7a1f20e98c98ef2c224`  
		Last Modified: Thu, 14 Aug 2025 20:56:55 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-alpine3.22`

```console
$ docker pull nats@sha256:71092f77d707a4a81b12aca5096d6b2d2e07ad16aa57c84066940a17af74f61a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:9e5633ac7584fc4e80d34be3ff7e15aa3fabec79a5573c2d9abefcf1f7761d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10586751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dfa54630538e8565a0953e5d7316c4b92bd17e293ec333e94f52be2094e7300`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ab6e8880f219a2dd7752796195d9939c137da1ea12c10015c60812ca497573`  
		Last Modified: Thu, 14 Aug 2025 17:21:49 GMT  
		Size: 6.8 MB (6786090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283833608b5ae7ddb376c701f296ad922908c7627de5632ba6e83601e7ac8355`  
		Last Modified: Thu, 14 Aug 2025 17:21:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3411c495c894b3b46ad114eceb39fb6deff204dacab199804c51fd2e1a33a5ae`  
		Last Modified: Thu, 14 Aug 2025 17:21:49 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:d90e427f49684d9b241e599c42a542365675aa62dd6d92a617694d503903cfcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299652c57abf36d15568386e529c8a81ada9d5600ced03a88bccc20b7a50be31`

```dockerfile
```

-	Layers:
	-	`sha256:4ff271d6ce9dacd8101fce3d16eda36e2bbe12422efe9c37df07a8f681004669`  
		Last Modified: Thu, 14 Aug 2025 17:56:25 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:2cfaa354cfe1d863108af5b170d266f632b75f3785be68158e9e0cd1170c640a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10004611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:decbc388e2e168ea436dfa71f5e8cac800997860eb2b021cab4f5e4eec76027f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381ebd5419e3fec8229c2bc4e50847a161b2d4865cfcb4e6733a0ea3c32c77b4`  
		Last Modified: Thu, 14 Aug 2025 18:30:15 GMT  
		Size: 6.5 MB (6502730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37fce2ec2d65289a1c9ac7f39b6ae87b35135e3b107484e7e844793f8d7ff565`  
		Last Modified: Thu, 14 Aug 2025 17:37:15 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872252a349b6a653af65ab2ffc9f0d3cf5eeca6d0e42153f5c303d068d5e1812`  
		Last Modified: Thu, 14 Aug 2025 17:37:18 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:14ef749c437d808301a1efe45e399507ff98890b94c616d0007f1534cc8ab482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac20fd9b620208d75d0fd87edc4b9f19c291e788b7e21cc16cbdb65e53dac741`

```dockerfile
```

-	Layers:
	-	`sha256:57504cb714044ba92951c29c12ec66ede4547725749d0a068268c4cb751a035d`  
		Last Modified: Thu, 14 Aug 2025 20:56:44 GMT  
		Size: 14.8 KB (14821 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:1dc6b44e4b33dbe327dda601fff6bb363ef44c34a4ab2177f307f2d9937f49a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9712521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8885fe376c67ec4357739c5950356acebf63efd04e908fdd24e82f77fbfc7511`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b47ccb42d9de5fae140120c5d63f9ac56f0c1a50c858bfdb2926a8b8c9fa01`  
		Last Modified: Thu, 14 Aug 2025 17:20:49 GMT  
		Size: 6.5 MB (6492514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ae165d2cd161f3b90c15a6ebf63ef30cd24b1314b6c1c9ccfdfe1929e38949`  
		Last Modified: Thu, 14 Aug 2025 17:20:49 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0ad244a682bc355346daaf39628ff905c5a9830e058a1e989c513f9abf0f34`  
		Last Modified: Thu, 14 Aug 2025 17:20:49 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:f63e9df6411bb2032dedb0fe108e98c278fa2dc1239ac4181f3aefe3dc522497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e855d196a62bbe9f94bd2c44e04b0d5cacb3afdcd63e28f775fa65001122f6a0`

```dockerfile
```

-	Layers:
	-	`sha256:d69e84adacba24383fb74725a58e3be312fd8246fa5942fd3aa8c1b8b60cc567`  
		Last Modified: Thu, 14 Aug 2025 17:56:31 GMT  
		Size: 14.8 KB (14821 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e2578c673d8e347750aad6968df9283d0902cf83b36f7f52eaa2c169fde4886c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10409365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21abd46018664ec1d774ed0ccf028420f6687e33f812018fc3a910dc1ce6014`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdc9114678c7494cfff4d6d27e8c14856724b7b46c06d21e6f5309bb10cfd3e`  
		Last Modified: Thu, 14 Aug 2025 18:48:38 GMT  
		Size: 6.3 MB (6277644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9345987e164f0a7a3c9724b12596354d6f5b27a55c274c5943cf749ce9826044`  
		Last Modified: Thu, 14 Aug 2025 18:48:37 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac90761c84b8f60ad18110b9e9ff4b720ab1d809ff03b57faf042e634d59447`  
		Last Modified: Thu, 14 Aug 2025 18:48:38 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5b917f85bbda7141f8205a4c9d33e28145986c0124ea61f249bd1dbddc4eb538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b21a2426a39cfaf66ebf67d14f2866bfd16bf48c2083eed033b2421bd386a90`

```dockerfile
```

-	Layers:
	-	`sha256:e7738d4b72278c061ab6dd0a6f25f99f4c87e2797157b8dac4f79cea46c6760a`  
		Last Modified: Thu, 14 Aug 2025 20:56:49 GMT  
		Size: 14.9 KB (14865 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:30ad03d77dfb5de88442d0f29c490713d82448efd77693faf7b0935a99453b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9985901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23f66326a77590bc41eb0a5f9f97a5c40ca317276be7cdaf7f7322df7416182`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3e45745642d3a22ccb49be50acc20c0214bd2a5273c0975019b6597df4b5d2`  
		Last Modified: Thu, 14 Aug 2025 18:56:45 GMT  
		Size: 6.3 MB (6257816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a20674adfb2e91f75f547789596c957e2840dfa110ac58dcec2f5e6b686fcd`  
		Last Modified: Thu, 14 Aug 2025 18:56:43 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f76e967ee5d9ae2c5527cef9bb9c8edd4f553ba6495330dc86ee3565f14fc6`  
		Last Modified: Thu, 14 Aug 2025 18:56:43 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:050addcc71308640a4197a465ab8b25fd37500d546c2fbade4232636badd6976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44be2d0d1465d7c59fd92abeb1e0ea0dc33b19b0122cfa12d0204c30e4d4ae13`

```dockerfile
```

-	Layers:
	-	`sha256:66f52a56e2b84f4136709b50caf6b3e34917205c3aeba573456e28d55213cdaa`  
		Last Modified: Thu, 14 Aug 2025 20:56:52 GMT  
		Size: 14.8 KB (14781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:2bf7f126291a09aa21ef2c65fc041fedfe9e9e29e16a8858bf193280e1318fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10271313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e03788a43a2cfeaefbb6d84b08849b6b847b39eeab7af6cfa746c5475cc49a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813401984db76a6756e0db9016fe48ee5c9d82865d147dd243a26b51b2aad684`  
		Last Modified: Thu, 14 Aug 2025 18:35:37 GMT  
		Size: 6.6 MB (6625370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968c785997911db8d7fa72cfc92186b2fc98d2dd5485d575df8bede6c19e3837`  
		Last Modified: Thu, 14 Aug 2025 18:35:38 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5213bbb60ea3349a52da162a1ed048b3650fabc2973bb84980b33601e46410af`  
		Last Modified: Thu, 14 Aug 2025 18:35:37 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:068c939c8d89bfd8a734c0c4fcb03e2f6122fb7cb278e2af5857d850feb3c05c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f0a7a9a995483ed6030887daaf0da034c453fa869bd81b7cb6c7e352c4e8daa`

```dockerfile
```

-	Layers:
	-	`sha256:4f8fbf204f658abfd1d495febd491047b4ab613c794be7a1f20e98c98ef2c224`  
		Last Modified: Thu, 14 Aug 2025 20:56:55 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-linux`

```console
$ docker pull nats@sha256:afa7b504a629a7e9f8b4a3984a4dd796fe58a5267adbe0c18af723277657af7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:5634002bb5af84b0379f0de363bf0027b76bd6cf1a1db66ad254ae945a163cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6340078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d63b90f51c086da0db2adbc1a2ad7102ecabb8fa67c2470fdc2217b40a4d922`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b663fe8cd396789f2474139e39527f819c3a482db5e25e230cacaadd75df18ce`  
		Last Modified: Thu, 14 Aug 2025 17:27:46 GMT  
		Size: 6.3 MB (6339570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e38b65a6463af6a5ebdc0b02115f51a91399b2710a2758586bbeda7b6d50ba`  
		Last Modified: Thu, 14 Aug 2025 17:27:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:2ab05007143b6795815ff8714f15842e070df35013849973ca0b2f3552177ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310bb9bbe1f9febd06c494bb2dd5b961d7bf71acc8bf0b2fb53e0834a8cc2117`

```dockerfile
```

-	Layers:
	-	`sha256:85acdef1c273fe4667fee682e56c38f81137085631f156c2949814b3bc0d0bee`  
		Last Modified: Thu, 14 Aug 2025 20:56:26 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:40d95d59739fe46433103f4d262d1dd789f75ee44e99c640ea6457cf05487501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6054066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492743618ce250d8b5f53bf5f1e12404d57c3ec44625d5b44726e86f9bba5086`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f10f27efc9fb4dc2b4cdaada3f99aa2ffb9ebc99496fd55f1920263e51b914c9`  
		Last Modified: Thu, 14 Aug 2025 18:07:33 GMT  
		Size: 6.1 MB (6053556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bdfede140a8dbbb6956c184b88de98cc1662ecbef253a2a4433bc47021d07dc`  
		Last Modified: Thu, 14 Aug 2025 18:07:33 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:06dde395a53d1e08b8fd585a2037a3d0579d0cf26446b77df720fb5c757064f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b6f621ca40cc0a37945b871d68296b32cdb51732868485359bc907292b6eba`

```dockerfile
```

-	Layers:
	-	`sha256:6cffdd7549f5659166afe24fb85e23cfebf2409e108e1f347151569e8e28ba38`  
		Last Modified: Thu, 14 Aug 2025 20:56:30 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:815e928020aef447482878a6cef15fd72ac0f9d767b8309b032f7fb8feb7a353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6043424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbbf5945fb4360c4f621c54027b1cb47034cc2fa4d455ccc3f90923c1fe13761`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ba52e77e96ac90555714325e16a7b63d377c42dbeec68ba24cd503063cf7b9e0`  
		Last Modified: Thu, 14 Aug 2025 17:27:10 GMT  
		Size: 6.0 MB (6042914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ee5e05524b58d5802a62546f6f2347446d5321c4e8d583722db5b777d831d1`  
		Last Modified: Thu, 14 Aug 2025 17:27:08 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:842f4f4569460f34fc562978f687fc36581c388b02ab14cdad623893d588f5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2b1c717567f7faa2dde66fcb89acd6dcf382ec81408e1c26ecb2d68f03d105`

```dockerfile
```

-	Layers:
	-	`sha256:62da1307e4b0132c952bdd53d1b82eb3e96fa2934b1b582a8b7277351ddc31cd`  
		Last Modified: Thu, 14 Aug 2025 20:56:33 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d46af1d33927787659e676ea4714a6d53c8ba71956e0cda595d30ab277af5341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b7bb1d1d30e4a8233087664e0b5540f3e42f49f27589cfb43d23bacbeb63ffe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5823b59d47a0c660012e09655022b6660ce21c617ee2978f3edacb2ac344cb9f`  
		Last Modified: Thu, 14 Aug 2025 19:46:02 GMT  
		Size: 5.8 MB (5827281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e915dc222e2df5e58849a12f73e5fcede2bc08f2c98fd12f234ad34883849b`  
		Last Modified: Thu, 14 Aug 2025 19:46:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:4e9ff58758ddaea565568a15d4d049d69f51f01f69e9e0e517c68718dfe93ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a92dc3160475131a9aa4330ac0e14dedb97f5d4d57d5a386b4b1033afe203bc`

```dockerfile
```

-	Layers:
	-	`sha256:efd6b414c46e44a7c6cd8407e5887b4066f7e91785d16647bdfc24cb7dfb35a4`  
		Last Modified: Thu, 14 Aug 2025 20:56:36 GMT  
		Size: 10.6 KB (10649 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:70ad109d17470e9dbefe10df2ea372ea487e5a28cf96934110c5f6e6b118c4ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5807845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcf49d098aee252cf17a17945623b98c12312f01460230bd2494a20949c2703`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:221614c6b4427295323da315f973992219d61abd51aa73f549b80d617ceed783`  
		Last Modified: Thu, 14 Aug 2025 20:45:44 GMT  
		Size: 5.8 MB (5807337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea070ca5e9aa9e1edaa1764d931a0b0e385793e5b3124004b4ba91da5efc9e9`  
		Last Modified: Thu, 14 Aug 2025 20:45:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:bf4cec841a590e736bc48410cd41b4eb5176b07e39b161d5827a0dfe411fb72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd14ce8eff83929fceb915b93bd248d9837b402d7c289ab095bb35b5306608d`

```dockerfile
```

-	Layers:
	-	`sha256:f968b5bb7ad9cd95b31e5948c6d247e8ff2820fa830ca084746ac40f662b15d1`  
		Last Modified: Thu, 14 Aug 2025 23:56:26 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:66e24c97e22fd4db570efbde5c154dad761a934509688d1066ff6faf16c6ff8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6173621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5239fb0f4852c75ada10240d6ad54ccabbe1c300c54385271ab0d9c9a16d599`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 Aug 2025 12:51:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 Aug 2025 12:51:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 Aug 2025 12:51:02 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 Aug 2025 12:51:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 Aug 2025 12:51:02 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 Aug 2025 12:51:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:84a200250dfb971cfcf23197670e7ccfcfae55787bc8842c737081462376b978`  
		Last Modified: Mon, 04 Aug 2025 18:10:15 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5013d749e0797d9a012b7f969383e42b359cae57b7b1945f62eae07e6f12bbb`  
		Last Modified: Mon, 04 Aug 2025 18:10:15 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:3e90c2e5acc844d0189d6d664df76b3fc55d6438e1be7c1146763d00098ed8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469d8c0a969e19358745ad9513225279dd13b3d004003729b94ccd524773ffb5`

```dockerfile
```

-	Layers:
	-	`sha256:3490df75b7ac2f5425cf2a5decc578d60f595e9e0317faa4e73c20548b16f138`  
		Last Modified: Mon, 04 Aug 2025 20:56:51 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:4b5bc1dda10956fffbd5637c74ca36f1f8e8999841816091381b80f7f4368b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2-nanoserver` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:ad9de8f09f3634777b25adb56728db4ae6804eb3e93cf167d338af2569150272
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129178975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3e567374bac2065f94b8560a0f1747b427e881b5faa654919d1f7abccc554d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Thu, 14 Aug 2025 18:14:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 14 Aug 2025 18:14:05 GMT
RUN cmd /S /C #(nop) COPY file:3fa3039439cf4074860757aeaaa6c458fcb2a8fd53320637e2edb93570462bde in C:\nats-server.exe 
# Thu, 14 Aug 2025 18:14:06 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Aug 2025 18:14:07 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 14 Aug 2025 18:14:08 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Aug 2025 18:14:09 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70dd762bbc2519848d92e4250ffd2e8ad506e67e2ccc6edb8b28deb7bd6a4cc3`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8303cc1b67f588378cd15d48f0f9092ea5f9e1d8e2832d99a509bdd9c8ff70a`  
		Last Modified: Thu, 14 Aug 2025 18:14:54 GMT  
		Size: 6.5 MB (6512850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5204fc3573607851e777581d8f3393c06877a1b385138e9ddb562e41c44ae04f`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5811e67cadd8e8c18aa9f537c4147610482318cb56ca5e6a1ff3cff5d96e4cfc`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b880e68edcdaf39200bd33cc61fd60fab56c1eae85a872652a20730da3d12a`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbef80910535149a3762e6bfc014c51084a8c11fa366889b246185411c39fb9`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:4b5bc1dda10956fffbd5637c74ca36f1f8e8999841816091381b80f7f4368b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:ad9de8f09f3634777b25adb56728db4ae6804eb3e93cf167d338af2569150272
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129178975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3e567374bac2065f94b8560a0f1747b427e881b5faa654919d1f7abccc554d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Thu, 14 Aug 2025 18:14:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 14 Aug 2025 18:14:05 GMT
RUN cmd /S /C #(nop) COPY file:3fa3039439cf4074860757aeaaa6c458fcb2a8fd53320637e2edb93570462bde in C:\nats-server.exe 
# Thu, 14 Aug 2025 18:14:06 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Aug 2025 18:14:07 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 14 Aug 2025 18:14:08 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Aug 2025 18:14:09 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70dd762bbc2519848d92e4250ffd2e8ad506e67e2ccc6edb8b28deb7bd6a4cc3`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8303cc1b67f588378cd15d48f0f9092ea5f9e1d8e2832d99a509bdd9c8ff70a`  
		Last Modified: Thu, 14 Aug 2025 18:14:54 GMT  
		Size: 6.5 MB (6512850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5204fc3573607851e777581d8f3393c06877a1b385138e9ddb562e41c44ae04f`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5811e67cadd8e8c18aa9f537c4147610482318cb56ca5e6a1ff3cff5d96e4cfc`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b880e68edcdaf39200bd33cc61fd60fab56c1eae85a872652a20730da3d12a`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbef80910535149a3762e6bfc014c51084a8c11fa366889b246185411c39fb9`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:afa7b504a629a7e9f8b4a3984a4dd796fe58a5267adbe0c18af723277657af7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:5634002bb5af84b0379f0de363bf0027b76bd6cf1a1db66ad254ae945a163cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6340078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d63b90f51c086da0db2adbc1a2ad7102ecabb8fa67c2470fdc2217b40a4d922`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b663fe8cd396789f2474139e39527f819c3a482db5e25e230cacaadd75df18ce`  
		Last Modified: Thu, 14 Aug 2025 17:27:46 GMT  
		Size: 6.3 MB (6339570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e38b65a6463af6a5ebdc0b02115f51a91399b2710a2758586bbeda7b6d50ba`  
		Last Modified: Thu, 14 Aug 2025 17:27:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:2ab05007143b6795815ff8714f15842e070df35013849973ca0b2f3552177ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310bb9bbe1f9febd06c494bb2dd5b961d7bf71acc8bf0b2fb53e0834a8cc2117`

```dockerfile
```

-	Layers:
	-	`sha256:85acdef1c273fe4667fee682e56c38f81137085631f156c2949814b3bc0d0bee`  
		Last Modified: Thu, 14 Aug 2025 20:56:26 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:40d95d59739fe46433103f4d262d1dd789f75ee44e99c640ea6457cf05487501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6054066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492743618ce250d8b5f53bf5f1e12404d57c3ec44625d5b44726e86f9bba5086`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f10f27efc9fb4dc2b4cdaada3f99aa2ffb9ebc99496fd55f1920263e51b914c9`  
		Last Modified: Thu, 14 Aug 2025 18:07:33 GMT  
		Size: 6.1 MB (6053556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bdfede140a8dbbb6956c184b88de98cc1662ecbef253a2a4433bc47021d07dc`  
		Last Modified: Thu, 14 Aug 2025 18:07:33 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:06dde395a53d1e08b8fd585a2037a3d0579d0cf26446b77df720fb5c757064f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b6f621ca40cc0a37945b871d68296b32cdb51732868485359bc907292b6eba`

```dockerfile
```

-	Layers:
	-	`sha256:6cffdd7549f5659166afe24fb85e23cfebf2409e108e1f347151569e8e28ba38`  
		Last Modified: Thu, 14 Aug 2025 20:56:30 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:815e928020aef447482878a6cef15fd72ac0f9d767b8309b032f7fb8feb7a353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6043424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbbf5945fb4360c4f621c54027b1cb47034cc2fa4d455ccc3f90923c1fe13761`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ba52e77e96ac90555714325e16a7b63d377c42dbeec68ba24cd503063cf7b9e0`  
		Last Modified: Thu, 14 Aug 2025 17:27:10 GMT  
		Size: 6.0 MB (6042914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ee5e05524b58d5802a62546f6f2347446d5321c4e8d583722db5b777d831d1`  
		Last Modified: Thu, 14 Aug 2025 17:27:08 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:842f4f4569460f34fc562978f687fc36581c388b02ab14cdad623893d588f5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2b1c717567f7faa2dde66fcb89acd6dcf382ec81408e1c26ecb2d68f03d105`

```dockerfile
```

-	Layers:
	-	`sha256:62da1307e4b0132c952bdd53d1b82eb3e96fa2934b1b582a8b7277351ddc31cd`  
		Last Modified: Thu, 14 Aug 2025 20:56:33 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d46af1d33927787659e676ea4714a6d53c8ba71956e0cda595d30ab277af5341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b7bb1d1d30e4a8233087664e0b5540f3e42f49f27589cfb43d23bacbeb63ffe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5823b59d47a0c660012e09655022b6660ce21c617ee2978f3edacb2ac344cb9f`  
		Last Modified: Thu, 14 Aug 2025 19:46:02 GMT  
		Size: 5.8 MB (5827281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e915dc222e2df5e58849a12f73e5fcede2bc08f2c98fd12f234ad34883849b`  
		Last Modified: Thu, 14 Aug 2025 19:46:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4e9ff58758ddaea565568a15d4d049d69f51f01f69e9e0e517c68718dfe93ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a92dc3160475131a9aa4330ac0e14dedb97f5d4d57d5a386b4b1033afe203bc`

```dockerfile
```

-	Layers:
	-	`sha256:efd6b414c46e44a7c6cd8407e5887b4066f7e91785d16647bdfc24cb7dfb35a4`  
		Last Modified: Thu, 14 Aug 2025 20:56:36 GMT  
		Size: 10.6 KB (10649 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:70ad109d17470e9dbefe10df2ea372ea487e5a28cf96934110c5f6e6b118c4ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5807845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcf49d098aee252cf17a17945623b98c12312f01460230bd2494a20949c2703`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:221614c6b4427295323da315f973992219d61abd51aa73f549b80d617ceed783`  
		Last Modified: Thu, 14 Aug 2025 20:45:44 GMT  
		Size: 5.8 MB (5807337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea070ca5e9aa9e1edaa1764d931a0b0e385793e5b3124004b4ba91da5efc9e9`  
		Last Modified: Thu, 14 Aug 2025 20:45:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:bf4cec841a590e736bc48410cd41b4eb5176b07e39b161d5827a0dfe411fb72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd14ce8eff83929fceb915b93bd248d9837b402d7c289ab095bb35b5306608d`

```dockerfile
```

-	Layers:
	-	`sha256:f968b5bb7ad9cd95b31e5948c6d247e8ff2820fa830ca084746ac40f662b15d1`  
		Last Modified: Thu, 14 Aug 2025 23:56:26 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:66e24c97e22fd4db570efbde5c154dad761a934509688d1066ff6faf16c6ff8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6173621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5239fb0f4852c75ada10240d6ad54ccabbe1c300c54385271ab0d9c9a16d599`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 Aug 2025 12:51:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 Aug 2025 12:51:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 Aug 2025 12:51:02 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 Aug 2025 12:51:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 Aug 2025 12:51:02 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 Aug 2025 12:51:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:84a200250dfb971cfcf23197670e7ccfcfae55787bc8842c737081462376b978`  
		Last Modified: Mon, 04 Aug 2025 18:10:15 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5013d749e0797d9a012b7f969383e42b359cae57b7b1945f62eae07e6f12bbb`  
		Last Modified: Mon, 04 Aug 2025 18:10:15 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:3e90c2e5acc844d0189d6d664df76b3fc55d6438e1be7c1146763d00098ed8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469d8c0a969e19358745ad9513225279dd13b3d004003729b94ccd524773ffb5`

```dockerfile
```

-	Layers:
	-	`sha256:3490df75b7ac2f5425cf2a5decc578d60f595e9e0317faa4e73c20548b16f138`  
		Last Modified: Mon, 04 Aug 2025 20:56:51 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:cd40ad4037d8bcb19778d0ec3407978059ea88d895747dfce3ea1be3f83f5760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2-windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:ff0d0047ceb610a0b73edcb6d12305bdf06e08a127258cf923e1aec9645ec419
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2288892735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe5b93e3cd45a63955014ff0d53cf5383f91b868d6bacf1c242ce4861d0a3fe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Thu, 14 Aug 2025 17:24:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 14 Aug 2025 17:24:18 GMT
ENV NATS_DOCKERIZED=1
# Thu, 14 Aug 2025 17:24:19 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 17:24:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.8/nats-server-v2.11.8-windows-amd64.zip
# Thu, 14 Aug 2025 17:24:21 GMT
ENV NATS_SERVER_SHASUM=3dd98465626e8c6ed92a784ef13c3f956c7e87fbbb4ee86cc198e377565eaeaf
# Thu, 14 Aug 2025 17:24:28 GMT
RUN Set-PSDebug -Trace 2
# Thu, 14 Aug 2025 17:24:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 14 Aug 2025 17:24:44 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Aug 2025 17:24:45 GMT
EXPOSE 4222 6222 8222
# Thu, 14 Aug 2025 17:24:46 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Aug 2025 17:24:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3f006d1cb294833347c0dcdeff82dda52af9acbea696337fd8408869317713`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e0fe1f9e451f5b78de6f2eabbcf9dd583e44cc8efca284c024e6fc31fea206`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4c9efb293cf4538944d58d49d978df5a06ed2586f43c0312291c6ed0854b98`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4fcdec518a7d5e9cbdbb2398711d526df04c6abd46f6dc74c91ce20cb62a28`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f32d8dbe729b86cde1eafd2da61359f32dab9aa4ff767aa70b3dc9351ba01c3`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1453289e44dd8e7a29b2a8395640bb6a2e2ebd47060a6bfe129031ce2072d7`  
		Last Modified: Thu, 14 Aug 2025 17:26:08 GMT  
		Size: 336.2 KB (336246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db38558f3d85860c055f99e79e865d42a17dd691a4f83ea93e0f8a5e391d125`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 6.9 MB (6852407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb87097b18d82c7dc42b80c5f6912e34cd08ecb316ffd445266fbb02ee18352b`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828b5772011538e3bb3bd9055b2b9e9b10bb6ffd46dc54a1d765d3e2dcfb03a6`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd3abb758a5b3c339001a04d7364df2b54b00e27711aecf5f44a76323ef676f`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366367ce039c79734b9ad15e13867ea0fd5f18ee46cc185dde59b3507a9b3392`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:cd40ad4037d8bcb19778d0ec3407978059ea88d895747dfce3ea1be3f83f5760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:ff0d0047ceb610a0b73edcb6d12305bdf06e08a127258cf923e1aec9645ec419
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2288892735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe5b93e3cd45a63955014ff0d53cf5383f91b868d6bacf1c242ce4861d0a3fe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Thu, 14 Aug 2025 17:24:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 14 Aug 2025 17:24:18 GMT
ENV NATS_DOCKERIZED=1
# Thu, 14 Aug 2025 17:24:19 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 17:24:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.8/nats-server-v2.11.8-windows-amd64.zip
# Thu, 14 Aug 2025 17:24:21 GMT
ENV NATS_SERVER_SHASUM=3dd98465626e8c6ed92a784ef13c3f956c7e87fbbb4ee86cc198e377565eaeaf
# Thu, 14 Aug 2025 17:24:28 GMT
RUN Set-PSDebug -Trace 2
# Thu, 14 Aug 2025 17:24:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 14 Aug 2025 17:24:44 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Aug 2025 17:24:45 GMT
EXPOSE 4222 6222 8222
# Thu, 14 Aug 2025 17:24:46 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Aug 2025 17:24:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3f006d1cb294833347c0dcdeff82dda52af9acbea696337fd8408869317713`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e0fe1f9e451f5b78de6f2eabbcf9dd583e44cc8efca284c024e6fc31fea206`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4c9efb293cf4538944d58d49d978df5a06ed2586f43c0312291c6ed0854b98`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4fcdec518a7d5e9cbdbb2398711d526df04c6abd46f6dc74c91ce20cb62a28`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f32d8dbe729b86cde1eafd2da61359f32dab9aa4ff767aa70b3dc9351ba01c3`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1453289e44dd8e7a29b2a8395640bb6a2e2ebd47060a6bfe129031ce2072d7`  
		Last Modified: Thu, 14 Aug 2025 17:26:08 GMT  
		Size: 336.2 KB (336246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db38558f3d85860c055f99e79e865d42a17dd691a4f83ea93e0f8a5e391d125`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 6.9 MB (6852407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb87097b18d82c7dc42b80c5f6912e34cd08ecb316ffd445266fbb02ee18352b`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828b5772011538e3bb3bd9055b2b9e9b10bb6ffd46dc54a1d765d3e2dcfb03a6`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd3abb758a5b3c339001a04d7364df2b54b00e27711aecf5f44a76323ef676f`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366367ce039c79734b9ad15e13867ea0fd5f18ee46cc185dde59b3507a9b3392`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10`

```console
$ docker pull nats@sha256:d7f4c3c9a9f33f55714d186653dabf6a267bdb7c01b6026ca52dcc6107cdd195
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.4052; amd64

### `nats:2.10` - linux; amd64

```console
$ docker pull nats@sha256:2a0409d5d335da088d5eb60f98e7882b60b0a9a5b92d6019d20c902ca7588a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ddcd15c359f8958615724ab9516d172d5c227639f64ce9f35be3262cb7da79`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 08 May 2025 17:10:43 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4364a6a0f24e73978066c4d6d2e9d0062d2f8b802888b683903b1fc2068c64e`  
		Last Modified: Tue, 15 Jul 2025 20:14:39 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:63653ba76d4d32980e19fd066d8faddf286d73c95386f032a558b8f086d7b18b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2fdaecafa45eb3f73e46dbc34d9df3bb65bee60d603a5d60c62a972015de3b`

```dockerfile
```

-	Layers:
	-	`sha256:47e5c127f32acda06d25e8984bf6a72c9eeb10f3035ba32c79598007166b4c04`  
		Last Modified: Tue, 15 Jul 2025 20:56:52 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm variant v6

```console
$ docker pull nats@sha256:9b1c04a34580e20c1490a5064e8313ffd4b360243c2e04857dac0a6007b498d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b89438d76c05402b8dcb01ac3e05140e48e6778392ec5a79304c8dc93c34ab4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Fri, 16 May 2025 18:30:15 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0b8dc5358e56de49c2f0e7716e74cea7e0fdf9dad7b6c8c0833946c48f1c04`  
		Last Modified: Wed, 16 Jul 2025 03:33:25 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:3c9ba3b9bad14f297514ccc78ada7e343c7fced17d13e93d2497e3b820e656b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af4cc263fe2872a74ad60773ac7449247b107114fff93d98730f326bc17f51a`

```dockerfile
```

-	Layers:
	-	`sha256:0864a387fb45608b88ada1923f0ae02f76ced72eaac759901ef8d413b49f0e90`  
		Last Modified: Wed, 16 Jul 2025 05:56:39 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm variant v7

```console
$ docker pull nats@sha256:f43f02525fb70177170f0a2fb9e79eb07268a953bd2a359059ad0900e9dd948a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b9ed2792726dc76d9bb645e33fc54558e17765d923750f2a8e3a9919fcca25`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Fri, 16 May 2025 18:30:26 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d14a1abdd14cd59fc3c35866ed467a8a919a44818f54633f7512bc4f7a582c`  
		Last Modified: Wed, 16 Jul 2025 03:33:48 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:0c5b7695979385addd534dbacd42e9f82510bec9b36c80c054c18b9c0186a88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f9deee6c48ab16a9d3566bf8a166d2644944751f3137e48eeaf1283d694789`

```dockerfile
```

-	Layers:
	-	`sha256:9e3d70c4c732b3cbdd09be6050262e51de8a8f3d1178c40928d72f9e5502c2d4`  
		Last Modified: Wed, 16 Jul 2025 05:56:42 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:21c647ab25a09241c0c78ef7f7e9ba6083a1b86fce0cd780c9af809d97ffddf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2056e89711a3040474edbcca6c618d45919dc6fd8987ebdea7a4b171555ab5f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 08 May 2025 19:09:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77beb0493669556ea4e0c29038c4cfd7004b5f18909b1b37246d478d36de2cd3`  
		Last Modified: Wed, 16 Jul 2025 05:54:41 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:906b93ff7ffb942ccf7a13492e018e5c3997bc804df0b25fb10696a5b7286d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07cc7ed8ae11f8d376966ddeda27149b7c5ac6600913c3720bbbd28e606bae1c`

```dockerfile
```

-	Layers:
	-	`sha256:537eba1a251d0b975fadebc4407648509a7eab6ec721314527899965013f8a1f`  
		Last Modified: Wed, 16 Jul 2025 08:56:41 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; ppc64le

```console
$ docker pull nats@sha256:014c8f26af1c8877d083639a4a71f3d28bdd2ef0cc1024f5abd5ad5a749dd614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af697dde1702417db0e603b104d59a0bf4fe45c849a705b0794315ff9eec71c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Tue, 03 Jun 2025 18:22:45 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d34bef1ba47a9f286f09257aa0f4d17538ad02c33480340aae3b37ea8299a9e`  
		Last Modified: Wed, 16 Jul 2025 01:28:38 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:8bec0a70d768c4a593813e084d564b8954cdbe9e39c3adc34ad2898b53b3d8bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd21f0f0a9dcfabb7da8c3fcdf06a25c98075abec4ea57d8701e21bea89c379`

```dockerfile
```

-	Layers:
	-	`sha256:4a14a68d1f067da5af8c833217be38b779e71337394b692aa00b00741d5400c7`  
		Last Modified: Wed, 16 Jul 2025 02:56:36 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - linux; s390x

```console
$ docker pull nats@sha256:229735ff9ae29b71a084efd4a55f69d41d306bef7efcfbd30696055c684849e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5739fdfecee9bc0f0f7c1d4f6cb2fb02729b2865faf92695668722c08f4f98`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Fri, 16 May 2025 21:50:26 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a9cae6c2299a407ee2d218121a975faced7a6ebeeec46936118a589e9ed1a6`  
		Last Modified: Wed, 16 Jul 2025 05:11:39 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10` - unknown; unknown

```console
$ docker pull nats@sha256:d700ae05354ed4cc0500126f0b484f359cd5dc9f04296ba0f1b9044970e41dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2ce57e3feadefdbd033fb8c954e6c285dcfe7902628243625856eedcdccd4d`

```dockerfile
```

-	Layers:
	-	`sha256:6a0f9c46d224878ea2592f9d8fb6ef61d616db89b5b2a21a3e4c750b584110e5`  
		Last Modified: Wed, 16 Jul 2025 08:56:45 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:cba783568678d1c68a2b4073b3b0be39ca405c92d6dc7f9ecad0c25a0574ef92
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (128964202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9385c305ac1f8866e295530083ffb02a2b3fd5d23cc3730a9f9b227e98b6a4ec`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:55:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Aug 2025 20:55:59 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Tue, 12 Aug 2025 20:56:01 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Aug 2025 20:56:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Aug 2025 20:56:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Aug 2025 20:56:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c837dddfcce083ad077931976a7f641ec93ba10083eda5f8a22bc7988a83ffc1`  
		Last Modified: Tue, 12 Aug 2025 20:56:52 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d489930ac4c4d391c4894a18fa2fff7d82d4e6d9605f17c81aef9502052645`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 6.3 MB (6298072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c90026a9e7ce0303106c2b5b46978da34dcb2de3af30c16266019b9034eec4`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfaf32e91dfc4db461e19c01c440ec241bf85ff811bee66e417553a76eea8058`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b107a9ceaaac29dcd37c5e1b8a1d6e58d19d0c7b63a17038544cd2748ee848ce`  
		Last Modified: Tue, 12 Aug 2025 20:56:55 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9900866d54f1143578377b44a19c9589852ed0f8ff45b1a12bd28fec9282514c`  
		Last Modified: Tue, 12 Aug 2025 20:56:55 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-alpine`

```console
$ docker pull nats@sha256:eca033f54dbb5d0a5df80c60ff229e53c71de63a8b4ddd0c2f04dd3e55d287df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10-alpine` - linux; amd64

```console
$ docker pull nats@sha256:820a97ef8a0e8e4b1f1c940c1fbf92e57ad548429dd20754de24ffe4f08996a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10428162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faad9be7ec221398a67b66fa5f6dc4afe4e24f62ff6a2860f3a914caf5172c90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c015b317061ba6cf363edd67bb9353c30207a61e58e505226168bc0da98afe`  
		Last Modified: Tue, 15 Jul 2025 19:13:20 GMT  
		Size: 6.6 MB (6627507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a97296c7fe6d9f4da2c4c2dde8e7b27ce58644942a70f97ce0622c116554dc7`  
		Last Modified: Tue, 15 Jul 2025 19:13:20 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7355fe018b748ae16c9a4bbdaa99767706e56854d8d0535fd5aa2f96fbde81`  
		Last Modified: Tue, 15 Jul 2025 19:13:20 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:2b30e09f1d5f9b8e841201cf1ac53ade8e643572c891218121424a8b792908b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ad2f85e296997148a5e7d39b4527ad05c5559df3691d711ac6d93cc2b2799a`

```dockerfile
```

-	Layers:
	-	`sha256:89817af9341cc2fe811ba2110f7ecca87b5b39105610d0abae9f3e3da0a9777a`  
		Last Modified: Tue, 15 Jul 2025 20:57:03 GMT  
		Size: 13.1 KB (13121 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:bbbd389071ab1d8d254eb3df7fa93150882b5229c3a99da9d4cdd9d9d9fb4954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9852288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa1eb6ecb82b890304acc50b41737e48830c07d6adb9d5457e9eccebadb3768`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acf1350211366512043db3b27f0e92a67c14e308e2f135f34345d30309834ba`  
		Last Modified: Tue, 15 Jul 2025 19:55:46 GMT  
		Size: 6.4 MB (6350410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a9e0e3d02f0321c18cfb1f4ca8cf20685fcdb82a54101021179760ffa1115b`  
		Last Modified: Tue, 15 Jul 2025 19:55:46 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1209aaaa768e3b746d249f5d8401d372e7d5523f3a4397dde59eb595e0962b`  
		Last Modified: Tue, 15 Jul 2025 19:55:46 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:18c88d88649738fbf3c7c2459ea047163f1256228fa7897077a0bf288dc884b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583d11b71658547861a6f90067c7fb4d97c2d27cf0a804fba09a4535f16249da`

```dockerfile
```

-	Layers:
	-	`sha256:cd47a78549dc53d5c15b84eef49a9ad57778519a088bfbdafa38ec0be31ce357`  
		Last Modified: Tue, 15 Jul 2025 20:57:06 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:bae5228a4b8fa7abf5b2d2daeda9617519e08cc86149630e7adde2141efeb3a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9559514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4262f443d7ff0a48649c5f56e9ea6b6fa4f198ea37b29733999f51ae562c8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0607845d0fa55bdc3e76e0de89b169dd06188e51f5b2fb955e7ed32ae35f2380`  
		Last Modified: Tue, 15 Jul 2025 19:34:22 GMT  
		Size: 6.3 MB (6339508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d0483d372ec00a330e5264b9f6e35c5d71ac4528d86a6a9584483bc0212031`  
		Last Modified: Tue, 15 Jul 2025 19:34:21 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5469ded3bdfb31968ff768c86467701029b614a24b30acd8b12cf171bd1e3ef`  
		Last Modified: Tue, 15 Jul 2025 19:34:21 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:9c07cf58635126d1738dbc4853752497aeb197c3bf272aa23efc136bf8f18a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e7a9555de683929fd2a60677efa3416e877cd39c83ddf52e88187ae583703e`

```dockerfile
```

-	Layers:
	-	`sha256:8108e75ff73bb20deeee1f58da34c3cadf06f927494ad913c09b75c63eba39d8`  
		Last Modified: Tue, 15 Jul 2025 20:57:09 GMT  
		Size: 13.2 KB (13197 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:517e9d2a336ceb5f7d2bb56e2e760a0e519bc17980d917a1249963124a3009c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10266149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d275fb226d388d4dd3a791d2935b9e666b0bdcbb308c9ed5c3c275b9a6bf1b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da79ae039b8d8ecfd0f25dc397e0f909bd174215282d35acdf1d652d2405163a`  
		Last Modified: Tue, 15 Jul 2025 19:55:26 GMT  
		Size: 6.1 MB (6134432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e331104b5a2920b354684dc09575a324baffa357a7f6d0f1fb72f295736c2`  
		Last Modified: Tue, 15 Jul 2025 19:55:24 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30985de1842eae4c1801550eefc16aa2dd11494d3b0d68b4bfd3eee8e477a969`  
		Last Modified: Tue, 15 Jul 2025 19:55:26 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:291485af4a8930aeb01d6b2901e705d4e95e732c6b9641951ec8a39056797e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fd0a95567de843d6b30ff329f17bec6a7025150f0bdedd1dc0e66e6d0ced35`

```dockerfile
```

-	Layers:
	-	`sha256:b32eee42ece80938b5d8ccfe8ec8ce549a3c23ba61b4dae5d47b2987444084d9`  
		Last Modified: Tue, 15 Jul 2025 20:57:12 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:9fbb7e16a173fecf7e21d9f680c8ad01db7223d9272eb7ce77f00d1e073343d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9839117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e963a992e85fc13c981c490490ffe14da51fb501d335d1ae9179347930be7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a422db94aea345dcc4b152e623d957565ff862281021eaf67ca3c633d51915ee`  
		Last Modified: Tue, 15 Jul 2025 19:44:16 GMT  
		Size: 6.1 MB (6111037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddd307c13a337a7bea13fe784ac75d29d42bdd8667556e52f5a0a9692b7a636`  
		Last Modified: Tue, 15 Jul 2025 19:44:15 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b6b324f57973538f4622138b68d8d07a706ab3d27a788fedb1d1363551490b`  
		Last Modified: Tue, 15 Jul 2025 19:44:15 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:406badf2d3ae772f4bd44c8d377c85c9ead5f36a96c9df85c4548e809c0d119f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18389ddb2de7441fcb4b0e971a1363544c7120e69b057660eb6fbdf1a4650407`

```dockerfile
```

-	Layers:
	-	`sha256:774987c353747896140a05754243761038dae43ae58535b71a2c4918f6e606b5`  
		Last Modified: Tue, 15 Jul 2025 20:57:15 GMT  
		Size: 13.2 KB (13166 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine` - linux; s390x

```console
$ docker pull nats@sha256:b1c180246efdee1f796387ed45c5d804ec3cdc7d0d99c9016ec73546545214de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10112489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcc2bff49a935d91e94697fcd60f34d6fc3b487d0a8b21fa6df89d5d5931e900`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1202729b6d9714c15f30c3dd1bea1d18add10323ffa34e9a0577e120356652d5`  
		Last Modified: Tue, 15 Jul 2025 19:41:46 GMT  
		Size: 6.5 MB (6466550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5991bdba51cef03218a54daaf3057e75284c051ef0be6579e0b4fd39f388f6`  
		Last Modified: Tue, 15 Jul 2025 19:41:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334bcc04ba509cb8cdcfc5c52d3fbcb603b47fd5f6678b6600f7aeb1616bf557`  
		Last Modified: Tue, 15 Jul 2025 19:41:46 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:2665ec030c93be192eb44bd8e0517cd08761cd3ad98038dd72a182d8e1fb1cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b807b6464060a5c291e852155161137fa6a827bec9628c68c3d7c21fff68186a`

```dockerfile
```

-	Layers:
	-	`sha256:24831b5b37fe96a1f1d2cf2e30b77d0e59b1acf33b9953bf9fe12643150cb44c`  
		Last Modified: Tue, 15 Jul 2025 20:57:19 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-alpine3.22`

```console
$ docker pull nats@sha256:eca033f54dbb5d0a5df80c60ff229e53c71de63a8b4ddd0c2f04dd3e55d287df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:820a97ef8a0e8e4b1f1c940c1fbf92e57ad548429dd20754de24ffe4f08996a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10428162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faad9be7ec221398a67b66fa5f6dc4afe4e24f62ff6a2860f3a914caf5172c90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c015b317061ba6cf363edd67bb9353c30207a61e58e505226168bc0da98afe`  
		Last Modified: Tue, 15 Jul 2025 19:13:20 GMT  
		Size: 6.6 MB (6627507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a97296c7fe6d9f4da2c4c2dde8e7b27ce58644942a70f97ce0622c116554dc7`  
		Last Modified: Tue, 15 Jul 2025 19:13:20 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7355fe018b748ae16c9a4bbdaa99767706e56854d8d0535fd5aa2f96fbde81`  
		Last Modified: Tue, 15 Jul 2025 19:13:20 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:2b30e09f1d5f9b8e841201cf1ac53ade8e643572c891218121424a8b792908b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ad2f85e296997148a5e7d39b4527ad05c5559df3691d711ac6d93cc2b2799a`

```dockerfile
```

-	Layers:
	-	`sha256:89817af9341cc2fe811ba2110f7ecca87b5b39105610d0abae9f3e3da0a9777a`  
		Last Modified: Tue, 15 Jul 2025 20:57:03 GMT  
		Size: 13.1 KB (13121 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:bbbd389071ab1d8d254eb3df7fa93150882b5229c3a99da9d4cdd9d9d9fb4954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9852288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa1eb6ecb82b890304acc50b41737e48830c07d6adb9d5457e9eccebadb3768`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acf1350211366512043db3b27f0e92a67c14e308e2f135f34345d30309834ba`  
		Last Modified: Tue, 15 Jul 2025 19:55:46 GMT  
		Size: 6.4 MB (6350410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a9e0e3d02f0321c18cfb1f4ca8cf20685fcdb82a54101021179760ffa1115b`  
		Last Modified: Tue, 15 Jul 2025 19:55:46 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1209aaaa768e3b746d249f5d8401d372e7d5523f3a4397dde59eb595e0962b`  
		Last Modified: Tue, 15 Jul 2025 19:55:46 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:18c88d88649738fbf3c7c2459ea047163f1256228fa7897077a0bf288dc884b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583d11b71658547861a6f90067c7fb4d97c2d27cf0a804fba09a4535f16249da`

```dockerfile
```

-	Layers:
	-	`sha256:cd47a78549dc53d5c15b84eef49a9ad57778519a088bfbdafa38ec0be31ce357`  
		Last Modified: Tue, 15 Jul 2025 20:57:06 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:bae5228a4b8fa7abf5b2d2daeda9617519e08cc86149630e7adde2141efeb3a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9559514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4262f443d7ff0a48649c5f56e9ea6b6fa4f198ea37b29733999f51ae562c8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0607845d0fa55bdc3e76e0de89b169dd06188e51f5b2fb955e7ed32ae35f2380`  
		Last Modified: Tue, 15 Jul 2025 19:34:22 GMT  
		Size: 6.3 MB (6339508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d0483d372ec00a330e5264b9f6e35c5d71ac4528d86a6a9584483bc0212031`  
		Last Modified: Tue, 15 Jul 2025 19:34:21 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5469ded3bdfb31968ff768c86467701029b614a24b30acd8b12cf171bd1e3ef`  
		Last Modified: Tue, 15 Jul 2025 19:34:21 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:9c07cf58635126d1738dbc4853752497aeb197c3bf272aa23efc136bf8f18a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e7a9555de683929fd2a60677efa3416e877cd39c83ddf52e88187ae583703e`

```dockerfile
```

-	Layers:
	-	`sha256:8108e75ff73bb20deeee1f58da34c3cadf06f927494ad913c09b75c63eba39d8`  
		Last Modified: Tue, 15 Jul 2025 20:57:09 GMT  
		Size: 13.2 KB (13197 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:517e9d2a336ceb5f7d2bb56e2e760a0e519bc17980d917a1249963124a3009c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10266149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d275fb226d388d4dd3a791d2935b9e666b0bdcbb308c9ed5c3c275b9a6bf1b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da79ae039b8d8ecfd0f25dc397e0f909bd174215282d35acdf1d652d2405163a`  
		Last Modified: Tue, 15 Jul 2025 19:55:26 GMT  
		Size: 6.1 MB (6134432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e331104b5a2920b354684dc09575a324baffa357a7f6d0f1fb72f295736c2`  
		Last Modified: Tue, 15 Jul 2025 19:55:24 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30985de1842eae4c1801550eefc16aa2dd11494d3b0d68b4bfd3eee8e477a969`  
		Last Modified: Tue, 15 Jul 2025 19:55:26 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:291485af4a8930aeb01d6b2901e705d4e95e732c6b9641951ec8a39056797e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fd0a95567de843d6b30ff329f17bec6a7025150f0bdedd1dc0e66e6d0ced35`

```dockerfile
```

-	Layers:
	-	`sha256:b32eee42ece80938b5d8ccfe8ec8ce549a3c23ba61b4dae5d47b2987444084d9`  
		Last Modified: Tue, 15 Jul 2025 20:57:12 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:9fbb7e16a173fecf7e21d9f680c8ad01db7223d9272eb7ce77f00d1e073343d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9839117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e963a992e85fc13c981c490490ffe14da51fb501d335d1ae9179347930be7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a422db94aea345dcc4b152e623d957565ff862281021eaf67ca3c633d51915ee`  
		Last Modified: Tue, 15 Jul 2025 19:44:16 GMT  
		Size: 6.1 MB (6111037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddd307c13a337a7bea13fe784ac75d29d42bdd8667556e52f5a0a9692b7a636`  
		Last Modified: Tue, 15 Jul 2025 19:44:15 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b6b324f57973538f4622138b68d8d07a706ab3d27a788fedb1d1363551490b`  
		Last Modified: Tue, 15 Jul 2025 19:44:15 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:406badf2d3ae772f4bd44c8d377c85c9ead5f36a96c9df85c4548e809c0d119f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18389ddb2de7441fcb4b0e971a1363544c7120e69b057660eb6fbdf1a4650407`

```dockerfile
```

-	Layers:
	-	`sha256:774987c353747896140a05754243761038dae43ae58535b71a2c4918f6e606b5`  
		Last Modified: Tue, 15 Jul 2025 20:57:15 GMT  
		Size: 13.2 KB (13166 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:b1c180246efdee1f796387ed45c5d804ec3cdc7d0d99c9016ec73546545214de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10112489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcc2bff49a935d91e94697fcd60f34d6fc3b487d0a8b21fa6df89d5d5931e900`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1202729b6d9714c15f30c3dd1bea1d18add10323ffa34e9a0577e120356652d5`  
		Last Modified: Tue, 15 Jul 2025 19:41:46 GMT  
		Size: 6.5 MB (6466550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5991bdba51cef03218a54daaf3057e75284c051ef0be6579e0b4fd39f388f6`  
		Last Modified: Tue, 15 Jul 2025 19:41:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334bcc04ba509cb8cdcfc5c52d3fbcb603b47fd5f6678b6600f7aeb1616bf557`  
		Last Modified: Tue, 15 Jul 2025 19:41:46 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:2665ec030c93be192eb44bd8e0517cd08761cd3ad98038dd72a182d8e1fb1cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b807b6464060a5c291e852155161137fa6a827bec9628c68c3d7c21fff68186a`

```dockerfile
```

-	Layers:
	-	`sha256:24831b5b37fe96a1f1d2cf2e30b77d0e59b1acf33b9953bf9fe12643150cb44c`  
		Last Modified: Tue, 15 Jul 2025 20:57:19 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-linux`

```console
$ docker pull nats@sha256:13bf7761f143a1a82892026489162b8699068d239af79e242292b600df83cd18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10-linux` - linux; amd64

```console
$ docker pull nats@sha256:2a0409d5d335da088d5eb60f98e7882b60b0a9a5b92d6019d20c902ca7588a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ddcd15c359f8958615724ab9516d172d5c227639f64ce9f35be3262cb7da79`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 08 May 2025 17:10:43 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4364a6a0f24e73978066c4d6d2e9d0062d2f8b802888b683903b1fc2068c64e`  
		Last Modified: Tue, 15 Jul 2025 20:14:39 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:63653ba76d4d32980e19fd066d8faddf286d73c95386f032a558b8f086d7b18b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2fdaecafa45eb3f73e46dbc34d9df3bb65bee60d603a5d60c62a972015de3b`

```dockerfile
```

-	Layers:
	-	`sha256:47e5c127f32acda06d25e8984bf6a72c9eeb10f3035ba32c79598007166b4c04`  
		Last Modified: Tue, 15 Jul 2025 20:56:52 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:9b1c04a34580e20c1490a5064e8313ffd4b360243c2e04857dac0a6007b498d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b89438d76c05402b8dcb01ac3e05140e48e6778392ec5a79304c8dc93c34ab4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Fri, 16 May 2025 18:30:15 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0b8dc5358e56de49c2f0e7716e74cea7e0fdf9dad7b6c8c0833946c48f1c04`  
		Last Modified: Wed, 16 Jul 2025 03:33:25 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:3c9ba3b9bad14f297514ccc78ada7e343c7fced17d13e93d2497e3b820e656b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af4cc263fe2872a74ad60773ac7449247b107114fff93d98730f326bc17f51a`

```dockerfile
```

-	Layers:
	-	`sha256:0864a387fb45608b88ada1923f0ae02f76ced72eaac759901ef8d413b49f0e90`  
		Last Modified: Wed, 16 Jul 2025 05:56:39 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:f43f02525fb70177170f0a2fb9e79eb07268a953bd2a359059ad0900e9dd948a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b9ed2792726dc76d9bb645e33fc54558e17765d923750f2a8e3a9919fcca25`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Fri, 16 May 2025 18:30:26 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d14a1abdd14cd59fc3c35866ed467a8a919a44818f54633f7512bc4f7a582c`  
		Last Modified: Wed, 16 Jul 2025 03:33:48 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:0c5b7695979385addd534dbacd42e9f82510bec9b36c80c054c18b9c0186a88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f9deee6c48ab16a9d3566bf8a166d2644944751f3137e48eeaf1283d694789`

```dockerfile
```

-	Layers:
	-	`sha256:9e3d70c4c732b3cbdd09be6050262e51de8a8f3d1178c40928d72f9e5502c2d4`  
		Last Modified: Wed, 16 Jul 2025 05:56:42 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:21c647ab25a09241c0c78ef7f7e9ba6083a1b86fce0cd780c9af809d97ffddf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2056e89711a3040474edbcca6c618d45919dc6fd8987ebdea7a4b171555ab5f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 08 May 2025 19:09:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77beb0493669556ea4e0c29038c4cfd7004b5f18909b1b37246d478d36de2cd3`  
		Last Modified: Wed, 16 Jul 2025 05:54:41 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:906b93ff7ffb942ccf7a13492e018e5c3997bc804df0b25fb10696a5b7286d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07cc7ed8ae11f8d376966ddeda27149b7c5ac6600913c3720bbbd28e606bae1c`

```dockerfile
```

-	Layers:
	-	`sha256:537eba1a251d0b975fadebc4407648509a7eab6ec721314527899965013f8a1f`  
		Last Modified: Wed, 16 Jul 2025 08:56:41 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:014c8f26af1c8877d083639a4a71f3d28bdd2ef0cc1024f5abd5ad5a749dd614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af697dde1702417db0e603b104d59a0bf4fe45c849a705b0794315ff9eec71c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Tue, 03 Jun 2025 18:22:45 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d34bef1ba47a9f286f09257aa0f4d17538ad02c33480340aae3b37ea8299a9e`  
		Last Modified: Wed, 16 Jul 2025 01:28:38 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:8bec0a70d768c4a593813e084d564b8954cdbe9e39c3adc34ad2898b53b3d8bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd21f0f0a9dcfabb7da8c3fcdf06a25c98075abec4ea57d8701e21bea89c379`

```dockerfile
```

-	Layers:
	-	`sha256:4a14a68d1f067da5af8c833217be38b779e71337394b692aa00b00741d5400c7`  
		Last Modified: Wed, 16 Jul 2025 02:56:36 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-linux` - linux; s390x

```console
$ docker pull nats@sha256:229735ff9ae29b71a084efd4a55f69d41d306bef7efcfbd30696055c684849e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5739fdfecee9bc0f0f7c1d4f6cb2fb02729b2865faf92695668722c08f4f98`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Fri, 16 May 2025 21:50:26 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a9cae6c2299a407ee2d218121a975faced7a6ebeeec46936118a589e9ed1a6`  
		Last Modified: Wed, 16 Jul 2025 05:11:39 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-linux` - unknown; unknown

```console
$ docker pull nats@sha256:d700ae05354ed4cc0500126f0b484f359cd5dc9f04296ba0f1b9044970e41dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2ce57e3feadefdbd033fb8c954e6c285dcfe7902628243625856eedcdccd4d`

```dockerfile
```

-	Layers:
	-	`sha256:6a0f9c46d224878ea2592f9d8fb6ef61d616db89b5b2a21a3e4c750b584110e5`  
		Last Modified: Wed, 16 Jul 2025 08:56:45 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-nanoserver`

```console
$ docker pull nats@sha256:937644ce140eeef6e00310097663bc72a3ebc6d7a9ba0fa15aeff4c1bb0870c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2.10-nanoserver` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:cba783568678d1c68a2b4073b3b0be39ca405c92d6dc7f9ecad0c25a0574ef92
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (128964202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9385c305ac1f8866e295530083ffb02a2b3fd5d23cc3730a9f9b227e98b6a4ec`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:55:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Aug 2025 20:55:59 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Tue, 12 Aug 2025 20:56:01 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Aug 2025 20:56:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Aug 2025 20:56:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Aug 2025 20:56:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c837dddfcce083ad077931976a7f641ec93ba10083eda5f8a22bc7988a83ffc1`  
		Last Modified: Tue, 12 Aug 2025 20:56:52 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d489930ac4c4d391c4894a18fa2fff7d82d4e6d9605f17c81aef9502052645`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 6.3 MB (6298072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c90026a9e7ce0303106c2b5b46978da34dcb2de3af30c16266019b9034eec4`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfaf32e91dfc4db461e19c01c440ec241bf85ff811bee66e417553a76eea8058`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b107a9ceaaac29dcd37c5e1b8a1d6e58d19d0c7b63a17038544cd2748ee848ce`  
		Last Modified: Tue, 12 Aug 2025 20:56:55 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9900866d54f1143578377b44a19c9589852ed0f8ff45b1a12bd28fec9282514c`  
		Last Modified: Tue, 12 Aug 2025 20:56:55 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:937644ce140eeef6e00310097663bc72a3ebc6d7a9ba0fa15aeff4c1bb0870c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2.10-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:cba783568678d1c68a2b4073b3b0be39ca405c92d6dc7f9ecad0c25a0574ef92
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (128964202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9385c305ac1f8866e295530083ffb02a2b3fd5d23cc3730a9f9b227e98b6a4ec`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:55:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Aug 2025 20:55:59 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Tue, 12 Aug 2025 20:56:01 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Aug 2025 20:56:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Aug 2025 20:56:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Aug 2025 20:56:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c837dddfcce083ad077931976a7f641ec93ba10083eda5f8a22bc7988a83ffc1`  
		Last Modified: Tue, 12 Aug 2025 20:56:52 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d489930ac4c4d391c4894a18fa2fff7d82d4e6d9605f17c81aef9502052645`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 6.3 MB (6298072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c90026a9e7ce0303106c2b5b46978da34dcb2de3af30c16266019b9034eec4`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfaf32e91dfc4db461e19c01c440ec241bf85ff811bee66e417553a76eea8058`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b107a9ceaaac29dcd37c5e1b8a1d6e58d19d0c7b63a17038544cd2748ee848ce`  
		Last Modified: Tue, 12 Aug 2025 20:56:55 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9900866d54f1143578377b44a19c9589852ed0f8ff45b1a12bd28fec9282514c`  
		Last Modified: Tue, 12 Aug 2025 20:56:55 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-scratch`

```console
$ docker pull nats@sha256:13bf7761f143a1a82892026489162b8699068d239af79e242292b600df83cd18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10-scratch` - linux; amd64

```console
$ docker pull nats@sha256:2a0409d5d335da088d5eb60f98e7882b60b0a9a5b92d6019d20c902ca7588a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ddcd15c359f8958615724ab9516d172d5c227639f64ce9f35be3262cb7da79`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 08 May 2025 17:10:43 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4364a6a0f24e73978066c4d6d2e9d0062d2f8b802888b683903b1fc2068c64e`  
		Last Modified: Tue, 15 Jul 2025 20:14:39 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:63653ba76d4d32980e19fd066d8faddf286d73c95386f032a558b8f086d7b18b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2fdaecafa45eb3f73e46dbc34d9df3bb65bee60d603a5d60c62a972015de3b`

```dockerfile
```

-	Layers:
	-	`sha256:47e5c127f32acda06d25e8984bf6a72c9eeb10f3035ba32c79598007166b4c04`  
		Last Modified: Tue, 15 Jul 2025 20:56:52 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:9b1c04a34580e20c1490a5064e8313ffd4b360243c2e04857dac0a6007b498d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b89438d76c05402b8dcb01ac3e05140e48e6778392ec5a79304c8dc93c34ab4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Fri, 16 May 2025 18:30:15 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0b8dc5358e56de49c2f0e7716e74cea7e0fdf9dad7b6c8c0833946c48f1c04`  
		Last Modified: Wed, 16 Jul 2025 03:33:25 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:3c9ba3b9bad14f297514ccc78ada7e343c7fced17d13e93d2497e3b820e656b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af4cc263fe2872a74ad60773ac7449247b107114fff93d98730f326bc17f51a`

```dockerfile
```

-	Layers:
	-	`sha256:0864a387fb45608b88ada1923f0ae02f76ced72eaac759901ef8d413b49f0e90`  
		Last Modified: Wed, 16 Jul 2025 05:56:39 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:f43f02525fb70177170f0a2fb9e79eb07268a953bd2a359059ad0900e9dd948a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b9ed2792726dc76d9bb645e33fc54558e17765d923750f2a8e3a9919fcca25`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Fri, 16 May 2025 18:30:26 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d14a1abdd14cd59fc3c35866ed467a8a919a44818f54633f7512bc4f7a582c`  
		Last Modified: Wed, 16 Jul 2025 03:33:48 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:0c5b7695979385addd534dbacd42e9f82510bec9b36c80c054c18b9c0186a88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f9deee6c48ab16a9d3566bf8a166d2644944751f3137e48eeaf1283d694789`

```dockerfile
```

-	Layers:
	-	`sha256:9e3d70c4c732b3cbdd09be6050262e51de8a8f3d1178c40928d72f9e5502c2d4`  
		Last Modified: Wed, 16 Jul 2025 05:56:42 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:21c647ab25a09241c0c78ef7f7e9ba6083a1b86fce0cd780c9af809d97ffddf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2056e89711a3040474edbcca6c618d45919dc6fd8987ebdea7a4b171555ab5f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 08 May 2025 19:09:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77beb0493669556ea4e0c29038c4cfd7004b5f18909b1b37246d478d36de2cd3`  
		Last Modified: Wed, 16 Jul 2025 05:54:41 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:906b93ff7ffb942ccf7a13492e018e5c3997bc804df0b25fb10696a5b7286d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07cc7ed8ae11f8d376966ddeda27149b7c5ac6600913c3720bbbd28e606bae1c`

```dockerfile
```

-	Layers:
	-	`sha256:537eba1a251d0b975fadebc4407648509a7eab6ec721314527899965013f8a1f`  
		Last Modified: Wed, 16 Jul 2025 08:56:41 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:014c8f26af1c8877d083639a4a71f3d28bdd2ef0cc1024f5abd5ad5a749dd614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af697dde1702417db0e603b104d59a0bf4fe45c849a705b0794315ff9eec71c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Tue, 03 Jun 2025 18:22:45 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d34bef1ba47a9f286f09257aa0f4d17538ad02c33480340aae3b37ea8299a9e`  
		Last Modified: Wed, 16 Jul 2025 01:28:38 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:8bec0a70d768c4a593813e084d564b8954cdbe9e39c3adc34ad2898b53b3d8bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd21f0f0a9dcfabb7da8c3fcdf06a25c98075abec4ea57d8701e21bea89c379`

```dockerfile
```

-	Layers:
	-	`sha256:4a14a68d1f067da5af8c833217be38b779e71337394b692aa00b00741d5400c7`  
		Last Modified: Wed, 16 Jul 2025 02:56:36 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10-scratch` - linux; s390x

```console
$ docker pull nats@sha256:229735ff9ae29b71a084efd4a55f69d41d306bef7efcfbd30696055c684849e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5739fdfecee9bc0f0f7c1d4f6cb2fb02729b2865faf92695668722c08f4f98`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Fri, 16 May 2025 21:50:26 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a9cae6c2299a407ee2d218121a975faced7a6ebeeec46936118a589e9ed1a6`  
		Last Modified: Wed, 16 Jul 2025 05:11:39 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d700ae05354ed4cc0500126f0b484f359cd5dc9f04296ba0f1b9044970e41dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2ce57e3feadefdbd033fb8c954e6c285dcfe7902628243625856eedcdccd4d`

```dockerfile
```

-	Layers:
	-	`sha256:6a0f9c46d224878ea2592f9d8fb6ef61d616db89b5b2a21a3e4c750b584110e5`  
		Last Modified: Wed, 16 Jul 2025 08:56:45 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10-windowsservercore`

```console
$ docker pull nats@sha256:29927408a93e7326852ef265c921ace9e759be2911e7ec85aede94eea816ccd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2.10-windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:be846b5e8cb605dcba06fd770098cce2af40380738f3441e14ae22104232c611
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2288662304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade757d73346c5e0022a2f188676344fa11a7fdea7fd404d05b5ee974ee4bbea`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:26:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 Aug 2025 20:27:01 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 Aug 2025 20:27:02 GMT
ENV NATS_SERVER=2.10.29
# Tue, 12 Aug 2025 20:27:04 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.29/nats-server-v2.10.29-windows-amd64.zip
# Tue, 12 Aug 2025 20:27:05 GMT
ENV NATS_SERVER_SHASUM=98657bf4d5a9ce44168c019ba6894cda8e22e6adc8798edc05c168db7262de29
# Tue, 12 Aug 2025 20:27:14 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 Aug 2025 20:27:31 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 12 Aug 2025 20:27:33 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Aug 2025 20:27:34 GMT
EXPOSE 4222 6222 8222
# Tue, 12 Aug 2025 20:27:35 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Aug 2025 20:27:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2a4c01281f1ae501db3064c77b77dbd9ffaaa260b46486f8dfc009cddbd8b1`  
		Last Modified: Tue, 12 Aug 2025 20:29:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296600cfec08efd5530d7fd473aed79a9561c64f71209ca66802d1175aa618a7`  
		Last Modified: Tue, 12 Aug 2025 20:29:15 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e4271830b813f72ed5591ee787565fcf2da4ad52b65853e264ff6e39283b6f`  
		Last Modified: Tue, 12 Aug 2025 20:29:15 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662fe2d5b041e59d112c112fb4fc64f3bb6955c72f220821fb2cae76230c695f`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa8dc0c5e39061acce001fc58e690668965a4ab3f56945e7bbdb2d136653bc6`  
		Last Modified: Tue, 12 Aug 2025 20:45:15 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d30b7bdca9af240eea67bcf4d4adf7623350dfe2c833446e0c9a29b9855480`  
		Last Modified: Tue, 12 Aug 2025 20:29:18 GMT  
		Size: 321.5 KB (321463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184936b767a8f9cb88d544108366787e9f5398b7c71da2dcbbd19e9d047e69a6`  
		Last Modified: Tue, 12 Aug 2025 20:29:05 GMT  
		Size: 6.6 MB (6636730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103f8877b3beef57c768abb7061975f50c76a237352bc576717f5868e9dcb113`  
		Last Modified: Tue, 12 Aug 2025 20:29:04 GMT  
		Size: 1.8 KB (1847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2585b97227de952538a0ea34cb493ca9f7a87004ebb054e0d5bd8cc1b9e409ca`  
		Last Modified: Tue, 12 Aug 2025 20:29:04 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66eee2932ebf82391707e464199109eac1d85673e4af6b9990443d1a798b3520`  
		Last Modified: Tue, 12 Aug 2025 20:29:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:853c197674c3d054317d51e5b282132553b510776d8f41da2e05945fa7d9b083`  
		Last Modified: Tue, 12 Aug 2025 20:29:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:29927408a93e7326852ef265c921ace9e759be2911e7ec85aede94eea816ccd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2.10-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:be846b5e8cb605dcba06fd770098cce2af40380738f3441e14ae22104232c611
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2288662304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade757d73346c5e0022a2f188676344fa11a7fdea7fd404d05b5ee974ee4bbea`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:26:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 Aug 2025 20:27:01 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 Aug 2025 20:27:02 GMT
ENV NATS_SERVER=2.10.29
# Tue, 12 Aug 2025 20:27:04 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.29/nats-server-v2.10.29-windows-amd64.zip
# Tue, 12 Aug 2025 20:27:05 GMT
ENV NATS_SERVER_SHASUM=98657bf4d5a9ce44168c019ba6894cda8e22e6adc8798edc05c168db7262de29
# Tue, 12 Aug 2025 20:27:14 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 Aug 2025 20:27:31 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 12 Aug 2025 20:27:33 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Aug 2025 20:27:34 GMT
EXPOSE 4222 6222 8222
# Tue, 12 Aug 2025 20:27:35 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Aug 2025 20:27:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2a4c01281f1ae501db3064c77b77dbd9ffaaa260b46486f8dfc009cddbd8b1`  
		Last Modified: Tue, 12 Aug 2025 20:29:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296600cfec08efd5530d7fd473aed79a9561c64f71209ca66802d1175aa618a7`  
		Last Modified: Tue, 12 Aug 2025 20:29:15 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e4271830b813f72ed5591ee787565fcf2da4ad52b65853e264ff6e39283b6f`  
		Last Modified: Tue, 12 Aug 2025 20:29:15 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662fe2d5b041e59d112c112fb4fc64f3bb6955c72f220821fb2cae76230c695f`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa8dc0c5e39061acce001fc58e690668965a4ab3f56945e7bbdb2d136653bc6`  
		Last Modified: Tue, 12 Aug 2025 20:45:15 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d30b7bdca9af240eea67bcf4d4adf7623350dfe2c833446e0c9a29b9855480`  
		Last Modified: Tue, 12 Aug 2025 20:29:18 GMT  
		Size: 321.5 KB (321463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184936b767a8f9cb88d544108366787e9f5398b7c71da2dcbbd19e9d047e69a6`  
		Last Modified: Tue, 12 Aug 2025 20:29:05 GMT  
		Size: 6.6 MB (6636730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103f8877b3beef57c768abb7061975f50c76a237352bc576717f5868e9dcb113`  
		Last Modified: Tue, 12 Aug 2025 20:29:04 GMT  
		Size: 1.8 KB (1847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2585b97227de952538a0ea34cb493ca9f7a87004ebb054e0d5bd8cc1b9e409ca`  
		Last Modified: Tue, 12 Aug 2025 20:29:04 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66eee2932ebf82391707e464199109eac1d85673e4af6b9990443d1a798b3520`  
		Last Modified: Tue, 12 Aug 2025 20:29:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:853c197674c3d054317d51e5b282132553b510776d8f41da2e05945fa7d9b083`  
		Last Modified: Tue, 12 Aug 2025 20:29:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.29`

```console
$ docker pull nats@sha256:d7f4c3c9a9f33f55714d186653dabf6a267bdb7c01b6026ca52dcc6107cdd195
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.4052; amd64

### `nats:2.10.29` - linux; amd64

```console
$ docker pull nats@sha256:2a0409d5d335da088d5eb60f98e7882b60b0a9a5b92d6019d20c902ca7588a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ddcd15c359f8958615724ab9516d172d5c227639f64ce9f35be3262cb7da79`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 08 May 2025 17:10:43 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4364a6a0f24e73978066c4d6d2e9d0062d2f8b802888b683903b1fc2068c64e`  
		Last Modified: Tue, 15 Jul 2025 20:14:39 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:63653ba76d4d32980e19fd066d8faddf286d73c95386f032a558b8f086d7b18b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2fdaecafa45eb3f73e46dbc34d9df3bb65bee60d603a5d60c62a972015de3b`

```dockerfile
```

-	Layers:
	-	`sha256:47e5c127f32acda06d25e8984bf6a72c9eeb10f3035ba32c79598007166b4c04`  
		Last Modified: Tue, 15 Jul 2025 20:56:52 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - linux; arm variant v6

```console
$ docker pull nats@sha256:9b1c04a34580e20c1490a5064e8313ffd4b360243c2e04857dac0a6007b498d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b89438d76c05402b8dcb01ac3e05140e48e6778392ec5a79304c8dc93c34ab4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Fri, 16 May 2025 18:30:15 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0b8dc5358e56de49c2f0e7716e74cea7e0fdf9dad7b6c8c0833946c48f1c04`  
		Last Modified: Wed, 16 Jul 2025 03:33:25 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:3c9ba3b9bad14f297514ccc78ada7e343c7fced17d13e93d2497e3b820e656b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af4cc263fe2872a74ad60773ac7449247b107114fff93d98730f326bc17f51a`

```dockerfile
```

-	Layers:
	-	`sha256:0864a387fb45608b88ada1923f0ae02f76ced72eaac759901ef8d413b49f0e90`  
		Last Modified: Wed, 16 Jul 2025 05:56:39 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - linux; arm variant v7

```console
$ docker pull nats@sha256:f43f02525fb70177170f0a2fb9e79eb07268a953bd2a359059ad0900e9dd948a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b9ed2792726dc76d9bb645e33fc54558e17765d923750f2a8e3a9919fcca25`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Fri, 16 May 2025 18:30:26 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d14a1abdd14cd59fc3c35866ed467a8a919a44818f54633f7512bc4f7a582c`  
		Last Modified: Wed, 16 Jul 2025 03:33:48 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:0c5b7695979385addd534dbacd42e9f82510bec9b36c80c054c18b9c0186a88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f9deee6c48ab16a9d3566bf8a166d2644944751f3137e48eeaf1283d694789`

```dockerfile
```

-	Layers:
	-	`sha256:9e3d70c4c732b3cbdd09be6050262e51de8a8f3d1178c40928d72f9e5502c2d4`  
		Last Modified: Wed, 16 Jul 2025 05:56:42 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:21c647ab25a09241c0c78ef7f7e9ba6083a1b86fce0cd780c9af809d97ffddf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2056e89711a3040474edbcca6c618d45919dc6fd8987ebdea7a4b171555ab5f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 08 May 2025 19:09:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77beb0493669556ea4e0c29038c4cfd7004b5f18909b1b37246d478d36de2cd3`  
		Last Modified: Wed, 16 Jul 2025 05:54:41 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:906b93ff7ffb942ccf7a13492e018e5c3997bc804df0b25fb10696a5b7286d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07cc7ed8ae11f8d376966ddeda27149b7c5ac6600913c3720bbbd28e606bae1c`

```dockerfile
```

-	Layers:
	-	`sha256:537eba1a251d0b975fadebc4407648509a7eab6ec721314527899965013f8a1f`  
		Last Modified: Wed, 16 Jul 2025 08:56:41 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - linux; ppc64le

```console
$ docker pull nats@sha256:014c8f26af1c8877d083639a4a71f3d28bdd2ef0cc1024f5abd5ad5a749dd614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af697dde1702417db0e603b104d59a0bf4fe45c849a705b0794315ff9eec71c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Tue, 03 Jun 2025 18:22:45 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d34bef1ba47a9f286f09257aa0f4d17538ad02c33480340aae3b37ea8299a9e`  
		Last Modified: Wed, 16 Jul 2025 01:28:38 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:8bec0a70d768c4a593813e084d564b8954cdbe9e39c3adc34ad2898b53b3d8bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd21f0f0a9dcfabb7da8c3fcdf06a25c98075abec4ea57d8701e21bea89c379`

```dockerfile
```

-	Layers:
	-	`sha256:4a14a68d1f067da5af8c833217be38b779e71337394b692aa00b00741d5400c7`  
		Last Modified: Wed, 16 Jul 2025 02:56:36 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - linux; s390x

```console
$ docker pull nats@sha256:229735ff9ae29b71a084efd4a55f69d41d306bef7efcfbd30696055c684849e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5739fdfecee9bc0f0f7c1d4f6cb2fb02729b2865faf92695668722c08f4f98`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Fri, 16 May 2025 21:50:26 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a9cae6c2299a407ee2d218121a975faced7a6ebeeec46936118a589e9ed1a6`  
		Last Modified: Wed, 16 Jul 2025 05:11:39 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29` - unknown; unknown

```console
$ docker pull nats@sha256:d700ae05354ed4cc0500126f0b484f359cd5dc9f04296ba0f1b9044970e41dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2ce57e3feadefdbd033fb8c954e6c285dcfe7902628243625856eedcdccd4d`

```dockerfile
```

-	Layers:
	-	`sha256:6a0f9c46d224878ea2592f9d8fb6ef61d616db89b5b2a21a3e4c750b584110e5`  
		Last Modified: Wed, 16 Jul 2025 08:56:45 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:cba783568678d1c68a2b4073b3b0be39ca405c92d6dc7f9ecad0c25a0574ef92
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (128964202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9385c305ac1f8866e295530083ffb02a2b3fd5d23cc3730a9f9b227e98b6a4ec`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:55:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Aug 2025 20:55:59 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Tue, 12 Aug 2025 20:56:01 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Aug 2025 20:56:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Aug 2025 20:56:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Aug 2025 20:56:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c837dddfcce083ad077931976a7f641ec93ba10083eda5f8a22bc7988a83ffc1`  
		Last Modified: Tue, 12 Aug 2025 20:56:52 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d489930ac4c4d391c4894a18fa2fff7d82d4e6d9605f17c81aef9502052645`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 6.3 MB (6298072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c90026a9e7ce0303106c2b5b46978da34dcb2de3af30c16266019b9034eec4`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfaf32e91dfc4db461e19c01c440ec241bf85ff811bee66e417553a76eea8058`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b107a9ceaaac29dcd37c5e1b8a1d6e58d19d0c7b63a17038544cd2748ee848ce`  
		Last Modified: Tue, 12 Aug 2025 20:56:55 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9900866d54f1143578377b44a19c9589852ed0f8ff45b1a12bd28fec9282514c`  
		Last Modified: Tue, 12 Aug 2025 20:56:55 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.29-alpine`

```console
$ docker pull nats@sha256:eca033f54dbb5d0a5df80c60ff229e53c71de63a8b4ddd0c2f04dd3e55d287df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10.29-alpine` - linux; amd64

```console
$ docker pull nats@sha256:820a97ef8a0e8e4b1f1c940c1fbf92e57ad548429dd20754de24ffe4f08996a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10428162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faad9be7ec221398a67b66fa5f6dc4afe4e24f62ff6a2860f3a914caf5172c90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c015b317061ba6cf363edd67bb9353c30207a61e58e505226168bc0da98afe`  
		Last Modified: Tue, 15 Jul 2025 19:13:20 GMT  
		Size: 6.6 MB (6627507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a97296c7fe6d9f4da2c4c2dde8e7b27ce58644942a70f97ce0622c116554dc7`  
		Last Modified: Tue, 15 Jul 2025 19:13:20 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7355fe018b748ae16c9a4bbdaa99767706e56854d8d0535fd5aa2f96fbde81`  
		Last Modified: Tue, 15 Jul 2025 19:13:20 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:2b30e09f1d5f9b8e841201cf1ac53ade8e643572c891218121424a8b792908b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ad2f85e296997148a5e7d39b4527ad05c5559df3691d711ac6d93cc2b2799a`

```dockerfile
```

-	Layers:
	-	`sha256:89817af9341cc2fe811ba2110f7ecca87b5b39105610d0abae9f3e3da0a9777a`  
		Last Modified: Tue, 15 Jul 2025 20:57:03 GMT  
		Size: 13.1 KB (13121 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:bbbd389071ab1d8d254eb3df7fa93150882b5229c3a99da9d4cdd9d9d9fb4954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9852288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa1eb6ecb82b890304acc50b41737e48830c07d6adb9d5457e9eccebadb3768`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acf1350211366512043db3b27f0e92a67c14e308e2f135f34345d30309834ba`  
		Last Modified: Tue, 15 Jul 2025 19:55:46 GMT  
		Size: 6.4 MB (6350410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a9e0e3d02f0321c18cfb1f4ca8cf20685fcdb82a54101021179760ffa1115b`  
		Last Modified: Tue, 15 Jul 2025 19:55:46 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1209aaaa768e3b746d249f5d8401d372e7d5523f3a4397dde59eb595e0962b`  
		Last Modified: Tue, 15 Jul 2025 19:55:46 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:18c88d88649738fbf3c7c2459ea047163f1256228fa7897077a0bf288dc884b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583d11b71658547861a6f90067c7fb4d97c2d27cf0a804fba09a4535f16249da`

```dockerfile
```

-	Layers:
	-	`sha256:cd47a78549dc53d5c15b84eef49a9ad57778519a088bfbdafa38ec0be31ce357`  
		Last Modified: Tue, 15 Jul 2025 20:57:06 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:bae5228a4b8fa7abf5b2d2daeda9617519e08cc86149630e7adde2141efeb3a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9559514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4262f443d7ff0a48649c5f56e9ea6b6fa4f198ea37b29733999f51ae562c8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0607845d0fa55bdc3e76e0de89b169dd06188e51f5b2fb955e7ed32ae35f2380`  
		Last Modified: Tue, 15 Jul 2025 19:34:22 GMT  
		Size: 6.3 MB (6339508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d0483d372ec00a330e5264b9f6e35c5d71ac4528d86a6a9584483bc0212031`  
		Last Modified: Tue, 15 Jul 2025 19:34:21 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5469ded3bdfb31968ff768c86467701029b614a24b30acd8b12cf171bd1e3ef`  
		Last Modified: Tue, 15 Jul 2025 19:34:21 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:9c07cf58635126d1738dbc4853752497aeb197c3bf272aa23efc136bf8f18a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e7a9555de683929fd2a60677efa3416e877cd39c83ddf52e88187ae583703e`

```dockerfile
```

-	Layers:
	-	`sha256:8108e75ff73bb20deeee1f58da34c3cadf06f927494ad913c09b75c63eba39d8`  
		Last Modified: Tue, 15 Jul 2025 20:57:09 GMT  
		Size: 13.2 KB (13197 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:517e9d2a336ceb5f7d2bb56e2e760a0e519bc17980d917a1249963124a3009c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10266149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d275fb226d388d4dd3a791d2935b9e666b0bdcbb308c9ed5c3c275b9a6bf1b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da79ae039b8d8ecfd0f25dc397e0f909bd174215282d35acdf1d652d2405163a`  
		Last Modified: Tue, 15 Jul 2025 19:55:26 GMT  
		Size: 6.1 MB (6134432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e331104b5a2920b354684dc09575a324baffa357a7f6d0f1fb72f295736c2`  
		Last Modified: Tue, 15 Jul 2025 19:55:24 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30985de1842eae4c1801550eefc16aa2dd11494d3b0d68b4bfd3eee8e477a969`  
		Last Modified: Tue, 15 Jul 2025 19:55:26 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:291485af4a8930aeb01d6b2901e705d4e95e732c6b9641951ec8a39056797e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fd0a95567de843d6b30ff329f17bec6a7025150f0bdedd1dc0e66e6d0ced35`

```dockerfile
```

-	Layers:
	-	`sha256:b32eee42ece80938b5d8ccfe8ec8ce549a3c23ba61b4dae5d47b2987444084d9`  
		Last Modified: Tue, 15 Jul 2025 20:57:12 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:9fbb7e16a173fecf7e21d9f680c8ad01db7223d9272eb7ce77f00d1e073343d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9839117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e963a992e85fc13c981c490490ffe14da51fb501d335d1ae9179347930be7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a422db94aea345dcc4b152e623d957565ff862281021eaf67ca3c633d51915ee`  
		Last Modified: Tue, 15 Jul 2025 19:44:16 GMT  
		Size: 6.1 MB (6111037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddd307c13a337a7bea13fe784ac75d29d42bdd8667556e52f5a0a9692b7a636`  
		Last Modified: Tue, 15 Jul 2025 19:44:15 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b6b324f57973538f4622138b68d8d07a706ab3d27a788fedb1d1363551490b`  
		Last Modified: Tue, 15 Jul 2025 19:44:15 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:406badf2d3ae772f4bd44c8d377c85c9ead5f36a96c9df85c4548e809c0d119f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18389ddb2de7441fcb4b0e971a1363544c7120e69b057660eb6fbdf1a4650407`

```dockerfile
```

-	Layers:
	-	`sha256:774987c353747896140a05754243761038dae43ae58535b71a2c4918f6e606b5`  
		Last Modified: Tue, 15 Jul 2025 20:57:15 GMT  
		Size: 13.2 KB (13166 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine` - linux; s390x

```console
$ docker pull nats@sha256:b1c180246efdee1f796387ed45c5d804ec3cdc7d0d99c9016ec73546545214de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10112489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcc2bff49a935d91e94697fcd60f34d6fc3b487d0a8b21fa6df89d5d5931e900`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1202729b6d9714c15f30c3dd1bea1d18add10323ffa34e9a0577e120356652d5`  
		Last Modified: Tue, 15 Jul 2025 19:41:46 GMT  
		Size: 6.5 MB (6466550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5991bdba51cef03218a54daaf3057e75284c051ef0be6579e0b4fd39f388f6`  
		Last Modified: Tue, 15 Jul 2025 19:41:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334bcc04ba509cb8cdcfc5c52d3fbcb603b47fd5f6678b6600f7aeb1616bf557`  
		Last Modified: Tue, 15 Jul 2025 19:41:46 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:2665ec030c93be192eb44bd8e0517cd08761cd3ad98038dd72a182d8e1fb1cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b807b6464060a5c291e852155161137fa6a827bec9628c68c3d7c21fff68186a`

```dockerfile
```

-	Layers:
	-	`sha256:24831b5b37fe96a1f1d2cf2e30b77d0e59b1acf33b9953bf9fe12643150cb44c`  
		Last Modified: Tue, 15 Jul 2025 20:57:19 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.29-alpine3.22`

```console
$ docker pull nats@sha256:eca033f54dbb5d0a5df80c60ff229e53c71de63a8b4ddd0c2f04dd3e55d287df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10.29-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:820a97ef8a0e8e4b1f1c940c1fbf92e57ad548429dd20754de24ffe4f08996a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10428162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faad9be7ec221398a67b66fa5f6dc4afe4e24f62ff6a2860f3a914caf5172c90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c015b317061ba6cf363edd67bb9353c30207a61e58e505226168bc0da98afe`  
		Last Modified: Tue, 15 Jul 2025 19:13:20 GMT  
		Size: 6.6 MB (6627507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a97296c7fe6d9f4da2c4c2dde8e7b27ce58644942a70f97ce0622c116554dc7`  
		Last Modified: Tue, 15 Jul 2025 19:13:20 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7355fe018b748ae16c9a4bbdaa99767706e56854d8d0535fd5aa2f96fbde81`  
		Last Modified: Tue, 15 Jul 2025 19:13:20 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:2b30e09f1d5f9b8e841201cf1ac53ade8e643572c891218121424a8b792908b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ad2f85e296997148a5e7d39b4527ad05c5559df3691d711ac6d93cc2b2799a`

```dockerfile
```

-	Layers:
	-	`sha256:89817af9341cc2fe811ba2110f7ecca87b5b39105610d0abae9f3e3da0a9777a`  
		Last Modified: Tue, 15 Jul 2025 20:57:03 GMT  
		Size: 13.1 KB (13121 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:bbbd389071ab1d8d254eb3df7fa93150882b5229c3a99da9d4cdd9d9d9fb4954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9852288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa1eb6ecb82b890304acc50b41737e48830c07d6adb9d5457e9eccebadb3768`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acf1350211366512043db3b27f0e92a67c14e308e2f135f34345d30309834ba`  
		Last Modified: Tue, 15 Jul 2025 19:55:46 GMT  
		Size: 6.4 MB (6350410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a9e0e3d02f0321c18cfb1f4ca8cf20685fcdb82a54101021179760ffa1115b`  
		Last Modified: Tue, 15 Jul 2025 19:55:46 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1209aaaa768e3b746d249f5d8401d372e7d5523f3a4397dde59eb595e0962b`  
		Last Modified: Tue, 15 Jul 2025 19:55:46 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:18c88d88649738fbf3c7c2459ea047163f1256228fa7897077a0bf288dc884b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583d11b71658547861a6f90067c7fb4d97c2d27cf0a804fba09a4535f16249da`

```dockerfile
```

-	Layers:
	-	`sha256:cd47a78549dc53d5c15b84eef49a9ad57778519a088bfbdafa38ec0be31ce357`  
		Last Modified: Tue, 15 Jul 2025 20:57:06 GMT  
		Size: 13.2 KB (13198 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:bae5228a4b8fa7abf5b2d2daeda9617519e08cc86149630e7adde2141efeb3a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9559514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4262f443d7ff0a48649c5f56e9ea6b6fa4f198ea37b29733999f51ae562c8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0607845d0fa55bdc3e76e0de89b169dd06188e51f5b2fb955e7ed32ae35f2380`  
		Last Modified: Tue, 15 Jul 2025 19:34:22 GMT  
		Size: 6.3 MB (6339508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d0483d372ec00a330e5264b9f6e35c5d71ac4528d86a6a9584483bc0212031`  
		Last Modified: Tue, 15 Jul 2025 19:34:21 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5469ded3bdfb31968ff768c86467701029b614a24b30acd8b12cf171bd1e3ef`  
		Last Modified: Tue, 15 Jul 2025 19:34:21 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:9c07cf58635126d1738dbc4853752497aeb197c3bf272aa23efc136bf8f18a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e7a9555de683929fd2a60677efa3416e877cd39c83ddf52e88187ae583703e`

```dockerfile
```

-	Layers:
	-	`sha256:8108e75ff73bb20deeee1f58da34c3cadf06f927494ad913c09b75c63eba39d8`  
		Last Modified: Tue, 15 Jul 2025 20:57:09 GMT  
		Size: 13.2 KB (13197 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:517e9d2a336ceb5f7d2bb56e2e760a0e519bc17980d917a1249963124a3009c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10266149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d275fb226d388d4dd3a791d2935b9e666b0bdcbb308c9ed5c3c275b9a6bf1b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da79ae039b8d8ecfd0f25dc397e0f909bd174215282d35acdf1d652d2405163a`  
		Last Modified: Tue, 15 Jul 2025 19:55:26 GMT  
		Size: 6.1 MB (6134432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5e331104b5a2920b354684dc09575a324baffa357a7f6d0f1fb72f295736c2`  
		Last Modified: Tue, 15 Jul 2025 19:55:24 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30985de1842eae4c1801550eefc16aa2dd11494d3b0d68b4bfd3eee8e477a969`  
		Last Modified: Tue, 15 Jul 2025 19:55:26 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:291485af4a8930aeb01d6b2901e705d4e95e732c6b9641951ec8a39056797e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fd0a95567de843d6b30ff329f17bec6a7025150f0bdedd1dc0e66e6d0ced35`

```dockerfile
```

-	Layers:
	-	`sha256:b32eee42ece80938b5d8ccfe8ec8ce549a3c23ba61b4dae5d47b2987444084d9`  
		Last Modified: Tue, 15 Jul 2025 20:57:12 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:9fbb7e16a173fecf7e21d9f680c8ad01db7223d9272eb7ce77f00d1e073343d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9839117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e963a992e85fc13c981c490490ffe14da51fb501d335d1ae9179347930be7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a422db94aea345dcc4b152e623d957565ff862281021eaf67ca3c633d51915ee`  
		Last Modified: Tue, 15 Jul 2025 19:44:16 GMT  
		Size: 6.1 MB (6111037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddd307c13a337a7bea13fe784ac75d29d42bdd8667556e52f5a0a9692b7a636`  
		Last Modified: Tue, 15 Jul 2025 19:44:15 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b6b324f57973538f4622138b68d8d07a706ab3d27a788fedb1d1363551490b`  
		Last Modified: Tue, 15 Jul 2025 19:44:15 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:406badf2d3ae772f4bd44c8d377c85c9ead5f36a96c9df85c4548e809c0d119f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18389ddb2de7441fcb4b0e971a1363544c7120e69b057660eb6fbdf1a4650407`

```dockerfile
```

-	Layers:
	-	`sha256:774987c353747896140a05754243761038dae43ae58535b71a2c4918f6e606b5`  
		Last Modified: Tue, 15 Jul 2025 20:57:15 GMT  
		Size: 13.2 KB (13166 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:b1c180246efdee1f796387ed45c5d804ec3cdc7d0d99c9016ec73546545214de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10112489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcc2bff49a935d91e94697fcd60f34d6fc3b487d0a8b21fa6df89d5d5931e900`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
ENV NATS_SERVER=2.10.29
# Tue, 01 Jul 2025 16:09:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='da4b27942ecfb4c5f0c54553d2e7f470ddda9d7581cfe8131b351a0e223ed401' ;; 		armhf) natsArch='arm6'; sha256='7b70fd23bfbd9efa7ca5edb5aa18fe33b07ff993ac86db06372af297bfaf6fab' ;; 		armv7) natsArch='arm7'; sha256='a59e7336a32ef78b0ca8bc3e6707a5770461d3f45c4c2f96cfef263f26eaefd5' ;; 		x86_64) natsArch='amd64'; sha256='e314da74a83a1d3876db8814c27eb990fe729640fd6452025b441bcede8390da' ;; 		x86) natsArch='386'; sha256='abc385394c19784558f7aa2f9770fe2daceb22cf95e3fa398c832590479396b0' ;; 		s390x) natsArch='s390x'; sha256='ee821b1eae8bb98a0d4603510a41613dd15afef244261a79da33515699d1aece' ;; 		ppc64le) natsArch='ppc64le'; sha256='31b0063d261e5d8c59396f8a3f9298ad80b36fd4bc370ce59e5d160f55a0fe46' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1202729b6d9714c15f30c3dd1bea1d18add10323ffa34e9a0577e120356652d5`  
		Last Modified: Tue, 15 Jul 2025 19:41:46 GMT  
		Size: 6.5 MB (6466550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5991bdba51cef03218a54daaf3057e75284c051ef0be6579e0b4fd39f388f6`  
		Last Modified: Tue, 15 Jul 2025 19:41:45 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334bcc04ba509cb8cdcfc5c52d3fbcb603b47fd5f6678b6600f7aeb1616bf557`  
		Last Modified: Tue, 15 Jul 2025 19:41:46 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:2665ec030c93be192eb44bd8e0517cd08761cd3ad98038dd72a182d8e1fb1cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 KB (13122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b807b6464060a5c291e852155161137fa6a827bec9628c68c3d7c21fff68186a`

```dockerfile
```

-	Layers:
	-	`sha256:24831b5b37fe96a1f1d2cf2e30b77d0e59b1acf33b9953bf9fe12643150cb44c`  
		Last Modified: Tue, 15 Jul 2025 20:57:19 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.29-linux`

```console
$ docker pull nats@sha256:13bf7761f143a1a82892026489162b8699068d239af79e242292b600df83cd18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10.29-linux` - linux; amd64

```console
$ docker pull nats@sha256:2a0409d5d335da088d5eb60f98e7882b60b0a9a5b92d6019d20c902ca7588a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ddcd15c359f8958615724ab9516d172d5c227639f64ce9f35be3262cb7da79`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 08 May 2025 17:10:43 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4364a6a0f24e73978066c4d6d2e9d0062d2f8b802888b683903b1fc2068c64e`  
		Last Modified: Tue, 15 Jul 2025 20:14:39 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:63653ba76d4d32980e19fd066d8faddf286d73c95386f032a558b8f086d7b18b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2fdaecafa45eb3f73e46dbc34d9df3bb65bee60d603a5d60c62a972015de3b`

```dockerfile
```

-	Layers:
	-	`sha256:47e5c127f32acda06d25e8984bf6a72c9eeb10f3035ba32c79598007166b4c04`  
		Last Modified: Tue, 15 Jul 2025 20:56:52 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:9b1c04a34580e20c1490a5064e8313ffd4b360243c2e04857dac0a6007b498d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b89438d76c05402b8dcb01ac3e05140e48e6778392ec5a79304c8dc93c34ab4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Fri, 16 May 2025 18:30:15 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0b8dc5358e56de49c2f0e7716e74cea7e0fdf9dad7b6c8c0833946c48f1c04`  
		Last Modified: Wed, 16 Jul 2025 03:33:25 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:3c9ba3b9bad14f297514ccc78ada7e343c7fced17d13e93d2497e3b820e656b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af4cc263fe2872a74ad60773ac7449247b107114fff93d98730f326bc17f51a`

```dockerfile
```

-	Layers:
	-	`sha256:0864a387fb45608b88ada1923f0ae02f76ced72eaac759901ef8d413b49f0e90`  
		Last Modified: Wed, 16 Jul 2025 05:56:39 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:f43f02525fb70177170f0a2fb9e79eb07268a953bd2a359059ad0900e9dd948a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b9ed2792726dc76d9bb645e33fc54558e17765d923750f2a8e3a9919fcca25`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Fri, 16 May 2025 18:30:26 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d14a1abdd14cd59fc3c35866ed467a8a919a44818f54633f7512bc4f7a582c`  
		Last Modified: Wed, 16 Jul 2025 03:33:48 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:0c5b7695979385addd534dbacd42e9f82510bec9b36c80c054c18b9c0186a88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f9deee6c48ab16a9d3566bf8a166d2644944751f3137e48eeaf1283d694789`

```dockerfile
```

-	Layers:
	-	`sha256:9e3d70c4c732b3cbdd09be6050262e51de8a8f3d1178c40928d72f9e5502c2d4`  
		Last Modified: Wed, 16 Jul 2025 05:56:42 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:21c647ab25a09241c0c78ef7f7e9ba6083a1b86fce0cd780c9af809d97ffddf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2056e89711a3040474edbcca6c618d45919dc6fd8987ebdea7a4b171555ab5f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 08 May 2025 19:09:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77beb0493669556ea4e0c29038c4cfd7004b5f18909b1b37246d478d36de2cd3`  
		Last Modified: Wed, 16 Jul 2025 05:54:41 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:906b93ff7ffb942ccf7a13492e018e5c3997bc804df0b25fb10696a5b7286d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07cc7ed8ae11f8d376966ddeda27149b7c5ac6600913c3720bbbd28e606bae1c`

```dockerfile
```

-	Layers:
	-	`sha256:537eba1a251d0b975fadebc4407648509a7eab6ec721314527899965013f8a1f`  
		Last Modified: Wed, 16 Jul 2025 08:56:41 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:014c8f26af1c8877d083639a4a71f3d28bdd2ef0cc1024f5abd5ad5a749dd614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af697dde1702417db0e603b104d59a0bf4fe45c849a705b0794315ff9eec71c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Tue, 03 Jun 2025 18:22:45 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d34bef1ba47a9f286f09257aa0f4d17538ad02c33480340aae3b37ea8299a9e`  
		Last Modified: Wed, 16 Jul 2025 01:28:38 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:8bec0a70d768c4a593813e084d564b8954cdbe9e39c3adc34ad2898b53b3d8bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd21f0f0a9dcfabb7da8c3fcdf06a25c98075abec4ea57d8701e21bea89c379`

```dockerfile
```

-	Layers:
	-	`sha256:4a14a68d1f067da5af8c833217be38b779e71337394b692aa00b00741d5400c7`  
		Last Modified: Wed, 16 Jul 2025 02:56:36 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-linux` - linux; s390x

```console
$ docker pull nats@sha256:229735ff9ae29b71a084efd4a55f69d41d306bef7efcfbd30696055c684849e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5739fdfecee9bc0f0f7c1d4f6cb2fb02729b2865faf92695668722c08f4f98`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Fri, 16 May 2025 21:50:26 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a9cae6c2299a407ee2d218121a975faced7a6ebeeec46936118a589e9ed1a6`  
		Last Modified: Wed, 16 Jul 2025 05:11:39 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-linux` - unknown; unknown

```console
$ docker pull nats@sha256:d700ae05354ed4cc0500126f0b484f359cd5dc9f04296ba0f1b9044970e41dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2ce57e3feadefdbd033fb8c954e6c285dcfe7902628243625856eedcdccd4d`

```dockerfile
```

-	Layers:
	-	`sha256:6a0f9c46d224878ea2592f9d8fb6ef61d616db89b5b2a21a3e4c750b584110e5`  
		Last Modified: Wed, 16 Jul 2025 08:56:45 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.29-nanoserver`

```console
$ docker pull nats@sha256:937644ce140eeef6e00310097663bc72a3ebc6d7a9ba0fa15aeff4c1bb0870c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2.10.29-nanoserver` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:cba783568678d1c68a2b4073b3b0be39ca405c92d6dc7f9ecad0c25a0574ef92
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (128964202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9385c305ac1f8866e295530083ffb02a2b3fd5d23cc3730a9f9b227e98b6a4ec`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:55:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Aug 2025 20:55:59 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Tue, 12 Aug 2025 20:56:01 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Aug 2025 20:56:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Aug 2025 20:56:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Aug 2025 20:56:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c837dddfcce083ad077931976a7f641ec93ba10083eda5f8a22bc7988a83ffc1`  
		Last Modified: Tue, 12 Aug 2025 20:56:52 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d489930ac4c4d391c4894a18fa2fff7d82d4e6d9605f17c81aef9502052645`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 6.3 MB (6298072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c90026a9e7ce0303106c2b5b46978da34dcb2de3af30c16266019b9034eec4`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfaf32e91dfc4db461e19c01c440ec241bf85ff811bee66e417553a76eea8058`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b107a9ceaaac29dcd37c5e1b8a1d6e58d19d0c7b63a17038544cd2748ee848ce`  
		Last Modified: Tue, 12 Aug 2025 20:56:55 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9900866d54f1143578377b44a19c9589852ed0f8ff45b1a12bd28fec9282514c`  
		Last Modified: Tue, 12 Aug 2025 20:56:55 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.29-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:937644ce140eeef6e00310097663bc72a3ebc6d7a9ba0fa15aeff4c1bb0870c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2.10.29-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:cba783568678d1c68a2b4073b3b0be39ca405c92d6dc7f9ecad0c25a0574ef92
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (128964202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9385c305ac1f8866e295530083ffb02a2b3fd5d23cc3730a9f9b227e98b6a4ec`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:55:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Tue, 12 Aug 2025 20:55:59 GMT
RUN cmd /S /C #(nop) COPY file:bb21984c00af4126d47cf9b70fdf7b84c717ed994c40bb29d038dee2b51961fd in C:\nats-server.exe 
# Tue, 12 Aug 2025 20:56:01 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Aug 2025 20:56:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Tue, 12 Aug 2025 20:56:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Aug 2025 20:56:04 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c837dddfcce083ad077931976a7f641ec93ba10083eda5f8a22bc7988a83ffc1`  
		Last Modified: Tue, 12 Aug 2025 20:56:52 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d489930ac4c4d391c4894a18fa2fff7d82d4e6d9605f17c81aef9502052645`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 6.3 MB (6298072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c90026a9e7ce0303106c2b5b46978da34dcb2de3af30c16266019b9034eec4`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 1.7 KB (1675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfaf32e91dfc4db461e19c01c440ec241bf85ff811bee66e417553a76eea8058`  
		Last Modified: Tue, 12 Aug 2025 20:56:54 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b107a9ceaaac29dcd37c5e1b8a1d6e58d19d0c7b63a17038544cd2748ee848ce`  
		Last Modified: Tue, 12 Aug 2025 20:56:55 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9900866d54f1143578377b44a19c9589852ed0f8ff45b1a12bd28fec9282514c`  
		Last Modified: Tue, 12 Aug 2025 20:56:55 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.29-scratch`

```console
$ docker pull nats@sha256:13bf7761f143a1a82892026489162b8699068d239af79e242292b600df83cd18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.10.29-scratch` - linux; amd64

```console
$ docker pull nats@sha256:2a0409d5d335da088d5eb60f98e7882b60b0a9a5b92d6019d20c902ca7588a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6177484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ddcd15c359f8958615724ab9516d172d5c227639f64ce9f35be3262cb7da79`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8dc9f8d83356623edd591cde47fb5accec9c91519bf5e2a2ecbaba378696eff7`  
		Last Modified: Thu, 08 May 2025 17:10:43 GMT  
		Size: 6.2 MB (6176976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4364a6a0f24e73978066c4d6d2e9d0062d2f8b802888b683903b1fc2068c64e`  
		Last Modified: Tue, 15 Jul 2025 20:14:39 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:63653ba76d4d32980e19fd066d8faddf286d73c95386f032a558b8f086d7b18b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2fdaecafa45eb3f73e46dbc34d9df3bb65bee60d603a5d60c62a972015de3b`

```dockerfile
```

-	Layers:
	-	`sha256:47e5c127f32acda06d25e8984bf6a72c9eeb10f3035ba32c79598007166b4c04`  
		Last Modified: Tue, 15 Jul 2025 20:56:52 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:9b1c04a34580e20c1490a5064e8313ffd4b360243c2e04857dac0a6007b498d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b89438d76c05402b8dcb01ac3e05140e48e6778392ec5a79304c8dc93c34ab4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fa5273ca4aaf95ea6e1b9ef46f70f073183aff4281d28d8beb2cad3ad7db3be3`  
		Last Modified: Fri, 16 May 2025 18:30:15 GMT  
		Size: 5.9 MB (5898165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0b8dc5358e56de49c2f0e7716e74cea7e0fdf9dad7b6c8c0833946c48f1c04`  
		Last Modified: Wed, 16 Jul 2025 03:33:25 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:3c9ba3b9bad14f297514ccc78ada7e343c7fced17d13e93d2497e3b820e656b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af4cc263fe2872a74ad60773ac7449247b107114fff93d98730f326bc17f51a`

```dockerfile
```

-	Layers:
	-	`sha256:0864a387fb45608b88ada1923f0ae02f76ced72eaac759901ef8d413b49f0e90`  
		Last Modified: Wed, 16 Jul 2025 05:56:39 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:f43f02525fb70177170f0a2fb9e79eb07268a953bd2a359059ad0900e9dd948a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b9ed2792726dc76d9bb645e33fc54558e17765d923750f2a8e3a9919fcca25`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:96db703f3604bf0b2cef9a96db8383d43ffbea468f6c97f6c80fceaf1c1651a4`  
		Last Modified: Fri, 16 May 2025 18:30:26 GMT  
		Size: 5.9 MB (5891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d14a1abdd14cd59fc3c35866ed467a8a919a44818f54633f7512bc4f7a582c`  
		Last Modified: Wed, 16 Jul 2025 03:33:48 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:0c5b7695979385addd534dbacd42e9f82510bec9b36c80c054c18b9c0186a88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f9deee6c48ab16a9d3566bf8a166d2644944751f3137e48eeaf1283d694789`

```dockerfile
```

-	Layers:
	-	`sha256:9e3d70c4c732b3cbdd09be6050262e51de8a8f3d1178c40928d72f9e5502c2d4`  
		Last Modified: Wed, 16 Jul 2025 05:56:42 GMT  
		Size: 8.8 KB (8790 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:21c647ab25a09241c0c78ef7f7e9ba6083a1b86fce0cd780c9af809d97ffddf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5682078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2056e89711a3040474edbcca6c618d45919dc6fd8987ebdea7a4b171555ab5f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d64d9bbebf62f0a051d5cb189e70e395bdec4ba36971b0623c1901afc064521b`  
		Last Modified: Thu, 08 May 2025 19:09:24 GMT  
		Size: 5.7 MB (5681568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77beb0493669556ea4e0c29038c4cfd7004b5f18909b1b37246d478d36de2cd3`  
		Last Modified: Wed, 16 Jul 2025 05:54:41 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:906b93ff7ffb942ccf7a13492e018e5c3997bc804df0b25fb10696a5b7286d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07cc7ed8ae11f8d376966ddeda27149b7c5ac6600913c3720bbbd28e606bae1c`

```dockerfile
```

-	Layers:
	-	`sha256:537eba1a251d0b975fadebc4407648509a7eab6ec721314527899965013f8a1f`  
		Last Modified: Wed, 16 Jul 2025 08:56:41 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:014c8f26af1c8877d083639a4a71f3d28bdd2ef0cc1024f5abd5ad5a749dd614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5663221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af697dde1702417db0e603b104d59a0bf4fe45c849a705b0794315ff9eec71c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e76cdc72f647f0d1048fbb0f93c63b0f9e298dc4deec33bc751f2e73cc25b242`  
		Last Modified: Tue, 03 Jun 2025 18:22:45 GMT  
		Size: 5.7 MB (5662712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d34bef1ba47a9f286f09257aa0f4d17538ad02c33480340aae3b37ea8299a9e`  
		Last Modified: Wed, 16 Jul 2025 01:28:38 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:8bec0a70d768c4a593813e084d564b8954cdbe9e39c3adc34ad2898b53b3d8bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 KB (8765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd21f0f0a9dcfabb7da8c3fcdf06a25c98075abec4ea57d8701e21bea89c379`

```dockerfile
```

-	Layers:
	-	`sha256:4a14a68d1f067da5af8c833217be38b779e71337394b692aa00b00741d5400c7`  
		Last Modified: Wed, 16 Jul 2025 02:56:36 GMT  
		Size: 8.8 KB (8765 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.10.29-scratch` - linux; s390x

```console
$ docker pull nats@sha256:229735ff9ae29b71a084efd4a55f69d41d306bef7efcfbd30696055c684849e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6017042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5739fdfecee9bc0f0f7c1d4f6cb2fb02729b2865faf92695668722c08f4f98`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:71e2057fb31b76a1d788a29c48a6123896f7635cfa0cf3d5f847199ff0e53e66`  
		Last Modified: Fri, 16 May 2025 21:50:26 GMT  
		Size: 6.0 MB (6016533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a9cae6c2299a407ee2d218121a975faced7a6ebeeec46936118a589e9ed1a6`  
		Last Modified: Wed, 16 Jul 2025 05:11:39 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.10.29-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d700ae05354ed4cc0500126f0b484f359cd5dc9f04296ba0f1b9044970e41dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.7 KB (8711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2ce57e3feadefdbd033fb8c954e6c285dcfe7902628243625856eedcdccd4d`

```dockerfile
```

-	Layers:
	-	`sha256:6a0f9c46d224878ea2592f9d8fb6ef61d616db89b5b2a21a3e4c750b584110e5`  
		Last Modified: Wed, 16 Jul 2025 08:56:45 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.10.29-windowsservercore`

```console
$ docker pull nats@sha256:29927408a93e7326852ef265c921ace9e759be2911e7ec85aede94eea816ccd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2.10.29-windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:be846b5e8cb605dcba06fd770098cce2af40380738f3441e14ae22104232c611
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2288662304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade757d73346c5e0022a2f188676344fa11a7fdea7fd404d05b5ee974ee4bbea`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:26:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 Aug 2025 20:27:01 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 Aug 2025 20:27:02 GMT
ENV NATS_SERVER=2.10.29
# Tue, 12 Aug 2025 20:27:04 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.29/nats-server-v2.10.29-windows-amd64.zip
# Tue, 12 Aug 2025 20:27:05 GMT
ENV NATS_SERVER_SHASUM=98657bf4d5a9ce44168c019ba6894cda8e22e6adc8798edc05c168db7262de29
# Tue, 12 Aug 2025 20:27:14 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 Aug 2025 20:27:31 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 12 Aug 2025 20:27:33 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Aug 2025 20:27:34 GMT
EXPOSE 4222 6222 8222
# Tue, 12 Aug 2025 20:27:35 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Aug 2025 20:27:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2a4c01281f1ae501db3064c77b77dbd9ffaaa260b46486f8dfc009cddbd8b1`  
		Last Modified: Tue, 12 Aug 2025 20:29:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296600cfec08efd5530d7fd473aed79a9561c64f71209ca66802d1175aa618a7`  
		Last Modified: Tue, 12 Aug 2025 20:29:15 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e4271830b813f72ed5591ee787565fcf2da4ad52b65853e264ff6e39283b6f`  
		Last Modified: Tue, 12 Aug 2025 20:29:15 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662fe2d5b041e59d112c112fb4fc64f3bb6955c72f220821fb2cae76230c695f`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa8dc0c5e39061acce001fc58e690668965a4ab3f56945e7bbdb2d136653bc6`  
		Last Modified: Tue, 12 Aug 2025 20:45:15 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d30b7bdca9af240eea67bcf4d4adf7623350dfe2c833446e0c9a29b9855480`  
		Last Modified: Tue, 12 Aug 2025 20:29:18 GMT  
		Size: 321.5 KB (321463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184936b767a8f9cb88d544108366787e9f5398b7c71da2dcbbd19e9d047e69a6`  
		Last Modified: Tue, 12 Aug 2025 20:29:05 GMT  
		Size: 6.6 MB (6636730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103f8877b3beef57c768abb7061975f50c76a237352bc576717f5868e9dcb113`  
		Last Modified: Tue, 12 Aug 2025 20:29:04 GMT  
		Size: 1.8 KB (1847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2585b97227de952538a0ea34cb493ca9f7a87004ebb054e0d5bd8cc1b9e409ca`  
		Last Modified: Tue, 12 Aug 2025 20:29:04 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66eee2932ebf82391707e464199109eac1d85673e4af6b9990443d1a798b3520`  
		Last Modified: Tue, 12 Aug 2025 20:29:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:853c197674c3d054317d51e5b282132553b510776d8f41da2e05945fa7d9b083`  
		Last Modified: Tue, 12 Aug 2025 20:29:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.10.29-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:29927408a93e7326852ef265c921ace9e759be2911e7ec85aede94eea816ccd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2.10.29-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:be846b5e8cb605dcba06fd770098cce2af40380738f3441e14ae22104232c611
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2288662304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade757d73346c5e0022a2f188676344fa11a7fdea7fd404d05b5ee974ee4bbea`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:26:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 Aug 2025 20:27:01 GMT
ENV NATS_DOCKERIZED=1
# Tue, 12 Aug 2025 20:27:02 GMT
ENV NATS_SERVER=2.10.29
# Tue, 12 Aug 2025 20:27:04 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.10.29/nats-server-v2.10.29-windows-amd64.zip
# Tue, 12 Aug 2025 20:27:05 GMT
ENV NATS_SERVER_SHASUM=98657bf4d5a9ce44168c019ba6894cda8e22e6adc8798edc05c168db7262de29
# Tue, 12 Aug 2025 20:27:14 GMT
RUN Set-PSDebug -Trace 2
# Tue, 12 Aug 2025 20:27:31 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Tue, 12 Aug 2025 20:27:33 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Tue, 12 Aug 2025 20:27:34 GMT
EXPOSE 4222 6222 8222
# Tue, 12 Aug 2025 20:27:35 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Tue, 12 Aug 2025 20:27:37 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2a4c01281f1ae501db3064c77b77dbd9ffaaa260b46486f8dfc009cddbd8b1`  
		Last Modified: Tue, 12 Aug 2025 20:29:14 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296600cfec08efd5530d7fd473aed79a9561c64f71209ca66802d1175aa618a7`  
		Last Modified: Tue, 12 Aug 2025 20:29:15 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e4271830b813f72ed5591ee787565fcf2da4ad52b65853e264ff6e39283b6f`  
		Last Modified: Tue, 12 Aug 2025 20:29:15 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662fe2d5b041e59d112c112fb4fc64f3bb6955c72f220821fb2cae76230c695f`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa8dc0c5e39061acce001fc58e690668965a4ab3f56945e7bbdb2d136653bc6`  
		Last Modified: Tue, 12 Aug 2025 20:45:15 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d30b7bdca9af240eea67bcf4d4adf7623350dfe2c833446e0c9a29b9855480`  
		Last Modified: Tue, 12 Aug 2025 20:29:18 GMT  
		Size: 321.5 KB (321463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184936b767a8f9cb88d544108366787e9f5398b7c71da2dcbbd19e9d047e69a6`  
		Last Modified: Tue, 12 Aug 2025 20:29:05 GMT  
		Size: 6.6 MB (6636730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103f8877b3beef57c768abb7061975f50c76a237352bc576717f5868e9dcb113`  
		Last Modified: Tue, 12 Aug 2025 20:29:04 GMT  
		Size: 1.8 KB (1847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2585b97227de952538a0ea34cb493ca9f7a87004ebb054e0d5bd8cc1b9e409ca`  
		Last Modified: Tue, 12 Aug 2025 20:29:04 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66eee2932ebf82391707e464199109eac1d85673e4af6b9990443d1a798b3520`  
		Last Modified: Tue, 12 Aug 2025 20:29:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:853c197674c3d054317d51e5b282132553b510776d8f41da2e05945fa7d9b083`  
		Last Modified: Tue, 12 Aug 2025 20:29:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11`

```console
$ docker pull nats@sha256:86e9fe3e8d887ea2c12322b4231c1f2f64e3c5b9917168198e1ab6c0fe16b222
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.4052; amd64

### `nats:2.11` - linux; amd64

```console
$ docker pull nats@sha256:5634002bb5af84b0379f0de363bf0027b76bd6cf1a1db66ad254ae945a163cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6340078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d63b90f51c086da0db2adbc1a2ad7102ecabb8fa67c2470fdc2217b40a4d922`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b663fe8cd396789f2474139e39527f819c3a482db5e25e230cacaadd75df18ce`  
		Last Modified: Thu, 14 Aug 2025 17:27:46 GMT  
		Size: 6.3 MB (6339570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e38b65a6463af6a5ebdc0b02115f51a91399b2710a2758586bbeda7b6d50ba`  
		Last Modified: Thu, 14 Aug 2025 17:27:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:2ab05007143b6795815ff8714f15842e070df35013849973ca0b2f3552177ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310bb9bbe1f9febd06c494bb2dd5b961d7bf71acc8bf0b2fb53e0834a8cc2117`

```dockerfile
```

-	Layers:
	-	`sha256:85acdef1c273fe4667fee682e56c38f81137085631f156c2949814b3bc0d0bee`  
		Last Modified: Thu, 14 Aug 2025 20:56:26 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm variant v6

```console
$ docker pull nats@sha256:40d95d59739fe46433103f4d262d1dd789f75ee44e99c640ea6457cf05487501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6054066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492743618ce250d8b5f53bf5f1e12404d57c3ec44625d5b44726e86f9bba5086`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f10f27efc9fb4dc2b4cdaada3f99aa2ffb9ebc99496fd55f1920263e51b914c9`  
		Last Modified: Thu, 14 Aug 2025 18:07:33 GMT  
		Size: 6.1 MB (6053556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bdfede140a8dbbb6956c184b88de98cc1662ecbef253a2a4433bc47021d07dc`  
		Last Modified: Thu, 14 Aug 2025 18:07:33 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:06dde395a53d1e08b8fd585a2037a3d0579d0cf26446b77df720fb5c757064f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b6f621ca40cc0a37945b871d68296b32cdb51732868485359bc907292b6eba`

```dockerfile
```

-	Layers:
	-	`sha256:6cffdd7549f5659166afe24fb85e23cfebf2409e108e1f347151569e8e28ba38`  
		Last Modified: Thu, 14 Aug 2025 20:56:30 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm variant v7

```console
$ docker pull nats@sha256:815e928020aef447482878a6cef15fd72ac0f9d767b8309b032f7fb8feb7a353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6043424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbbf5945fb4360c4f621c54027b1cb47034cc2fa4d455ccc3f90923c1fe13761`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ba52e77e96ac90555714325e16a7b63d377c42dbeec68ba24cd503063cf7b9e0`  
		Last Modified: Thu, 14 Aug 2025 17:27:10 GMT  
		Size: 6.0 MB (6042914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ee5e05524b58d5802a62546f6f2347446d5321c4e8d583722db5b777d831d1`  
		Last Modified: Thu, 14 Aug 2025 17:27:08 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:842f4f4569460f34fc562978f687fc36581c388b02ab14cdad623893d588f5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2b1c717567f7faa2dde66fcb89acd6dcf382ec81408e1c26ecb2d68f03d105`

```dockerfile
```

-	Layers:
	-	`sha256:62da1307e4b0132c952bdd53d1b82eb3e96fa2934b1b582a8b7277351ddc31cd`  
		Last Modified: Thu, 14 Aug 2025 20:56:33 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d46af1d33927787659e676ea4714a6d53c8ba71956e0cda595d30ab277af5341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b7bb1d1d30e4a8233087664e0b5540f3e42f49f27589cfb43d23bacbeb63ffe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5823b59d47a0c660012e09655022b6660ce21c617ee2978f3edacb2ac344cb9f`  
		Last Modified: Thu, 14 Aug 2025 19:46:02 GMT  
		Size: 5.8 MB (5827281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e915dc222e2df5e58849a12f73e5fcede2bc08f2c98fd12f234ad34883849b`  
		Last Modified: Thu, 14 Aug 2025 19:46:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:4e9ff58758ddaea565568a15d4d049d69f51f01f69e9e0e517c68718dfe93ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a92dc3160475131a9aa4330ac0e14dedb97f5d4d57d5a386b4b1033afe203bc`

```dockerfile
```

-	Layers:
	-	`sha256:efd6b414c46e44a7c6cd8407e5887b4066f7e91785d16647bdfc24cb7dfb35a4`  
		Last Modified: Thu, 14 Aug 2025 20:56:36 GMT  
		Size: 10.6 KB (10649 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; ppc64le

```console
$ docker pull nats@sha256:70ad109d17470e9dbefe10df2ea372ea487e5a28cf96934110c5f6e6b118c4ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5807845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcf49d098aee252cf17a17945623b98c12312f01460230bd2494a20949c2703`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:221614c6b4427295323da315f973992219d61abd51aa73f549b80d617ceed783`  
		Last Modified: Thu, 14 Aug 2025 20:45:44 GMT  
		Size: 5.8 MB (5807337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea070ca5e9aa9e1edaa1764d931a0b0e385793e5b3124004b4ba91da5efc9e9`  
		Last Modified: Thu, 14 Aug 2025 20:45:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:bf4cec841a590e736bc48410cd41b4eb5176b07e39b161d5827a0dfe411fb72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd14ce8eff83929fceb915b93bd248d9837b402d7c289ab095bb35b5306608d`

```dockerfile
```

-	Layers:
	-	`sha256:f968b5bb7ad9cd95b31e5948c6d247e8ff2820fa830ca084746ac40f662b15d1`  
		Last Modified: Thu, 14 Aug 2025 23:56:26 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - linux; s390x

```console
$ docker pull nats@sha256:66e24c97e22fd4db570efbde5c154dad761a934509688d1066ff6faf16c6ff8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6173621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5239fb0f4852c75ada10240d6ad54ccabbe1c300c54385271ab0d9c9a16d599`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 Aug 2025 12:51:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 Aug 2025 12:51:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 Aug 2025 12:51:02 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 Aug 2025 12:51:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 Aug 2025 12:51:02 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 Aug 2025 12:51:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:84a200250dfb971cfcf23197670e7ccfcfae55787bc8842c737081462376b978`  
		Last Modified: Mon, 04 Aug 2025 18:10:15 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5013d749e0797d9a012b7f969383e42b359cae57b7b1945f62eae07e6f12bbb`  
		Last Modified: Mon, 04 Aug 2025 18:10:15 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11` - unknown; unknown

```console
$ docker pull nats@sha256:3e90c2e5acc844d0189d6d664df76b3fc55d6438e1be7c1146763d00098ed8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469d8c0a969e19358745ad9513225279dd13b3d004003729b94ccd524773ffb5`

```dockerfile
```

-	Layers:
	-	`sha256:3490df75b7ac2f5425cf2a5decc578d60f595e9e0317faa4e73c20548b16f138`  
		Last Modified: Mon, 04 Aug 2025 20:56:51 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:ad9de8f09f3634777b25adb56728db4ae6804eb3e93cf167d338af2569150272
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129178975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3e567374bac2065f94b8560a0f1747b427e881b5faa654919d1f7abccc554d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Thu, 14 Aug 2025 18:14:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 14 Aug 2025 18:14:05 GMT
RUN cmd /S /C #(nop) COPY file:3fa3039439cf4074860757aeaaa6c458fcb2a8fd53320637e2edb93570462bde in C:\nats-server.exe 
# Thu, 14 Aug 2025 18:14:06 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Aug 2025 18:14:07 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 14 Aug 2025 18:14:08 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Aug 2025 18:14:09 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70dd762bbc2519848d92e4250ffd2e8ad506e67e2ccc6edb8b28deb7bd6a4cc3`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8303cc1b67f588378cd15d48f0f9092ea5f9e1d8e2832d99a509bdd9c8ff70a`  
		Last Modified: Thu, 14 Aug 2025 18:14:54 GMT  
		Size: 6.5 MB (6512850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5204fc3573607851e777581d8f3393c06877a1b385138e9ddb562e41c44ae04f`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5811e67cadd8e8c18aa9f537c4147610482318cb56ca5e6a1ff3cff5d96e4cfc`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b880e68edcdaf39200bd33cc61fd60fab56c1eae85a872652a20730da3d12a`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbef80910535149a3762e6bfc014c51084a8c11fa366889b246185411c39fb9`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-alpine`

```console
$ docker pull nats@sha256:71092f77d707a4a81b12aca5096d6b2d2e07ad16aa57c84066940a17af74f61a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.11-alpine` - linux; amd64

```console
$ docker pull nats@sha256:9e5633ac7584fc4e80d34be3ff7e15aa3fabec79a5573c2d9abefcf1f7761d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10586751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dfa54630538e8565a0953e5d7316c4b92bd17e293ec333e94f52be2094e7300`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ab6e8880f219a2dd7752796195d9939c137da1ea12c10015c60812ca497573`  
		Last Modified: Thu, 14 Aug 2025 17:21:49 GMT  
		Size: 6.8 MB (6786090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283833608b5ae7ddb376c701f296ad922908c7627de5632ba6e83601e7ac8355`  
		Last Modified: Thu, 14 Aug 2025 17:21:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3411c495c894b3b46ad114eceb39fb6deff204dacab199804c51fd2e1a33a5ae`  
		Last Modified: Thu, 14 Aug 2025 17:21:49 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d90e427f49684d9b241e599c42a542365675aa62dd6d92a617694d503903cfcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299652c57abf36d15568386e529c8a81ada9d5600ced03a88bccc20b7a50be31`

```dockerfile
```

-	Layers:
	-	`sha256:4ff271d6ce9dacd8101fce3d16eda36e2bbe12422efe9c37df07a8f681004669`  
		Last Modified: Thu, 14 Aug 2025 17:56:25 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:2cfaa354cfe1d863108af5b170d266f632b75f3785be68158e9e0cd1170c640a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10004611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:decbc388e2e168ea436dfa71f5e8cac800997860eb2b021cab4f5e4eec76027f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381ebd5419e3fec8229c2bc4e50847a161b2d4865cfcb4e6733a0ea3c32c77b4`  
		Last Modified: Thu, 14 Aug 2025 18:30:15 GMT  
		Size: 6.5 MB (6502730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37fce2ec2d65289a1c9ac7f39b6ae87b35135e3b107484e7e844793f8d7ff565`  
		Last Modified: Thu, 14 Aug 2025 17:37:15 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872252a349b6a653af65ab2ffc9f0d3cf5eeca6d0e42153f5c303d068d5e1812`  
		Last Modified: Thu, 14 Aug 2025 17:37:18 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:14ef749c437d808301a1efe45e399507ff98890b94c616d0007f1534cc8ab482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac20fd9b620208d75d0fd87edc4b9f19c291e788b7e21cc16cbdb65e53dac741`

```dockerfile
```

-	Layers:
	-	`sha256:57504cb714044ba92951c29c12ec66ede4547725749d0a068268c4cb751a035d`  
		Last Modified: Thu, 14 Aug 2025 20:56:44 GMT  
		Size: 14.8 KB (14821 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:1dc6b44e4b33dbe327dda601fff6bb363ef44c34a4ab2177f307f2d9937f49a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9712521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8885fe376c67ec4357739c5950356acebf63efd04e908fdd24e82f77fbfc7511`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b47ccb42d9de5fae140120c5d63f9ac56f0c1a50c858bfdb2926a8b8c9fa01`  
		Last Modified: Thu, 14 Aug 2025 17:20:49 GMT  
		Size: 6.5 MB (6492514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ae165d2cd161f3b90c15a6ebf63ef30cd24b1314b6c1c9ccfdfe1929e38949`  
		Last Modified: Thu, 14 Aug 2025 17:20:49 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0ad244a682bc355346daaf39628ff905c5a9830e058a1e989c513f9abf0f34`  
		Last Modified: Thu, 14 Aug 2025 17:20:49 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f63e9df6411bb2032dedb0fe108e98c278fa2dc1239ac4181f3aefe3dc522497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e855d196a62bbe9f94bd2c44e04b0d5cacb3afdcd63e28f775fa65001122f6a0`

```dockerfile
```

-	Layers:
	-	`sha256:d69e84adacba24383fb74725a58e3be312fd8246fa5942fd3aa8c1b8b60cc567`  
		Last Modified: Thu, 14 Aug 2025 17:56:31 GMT  
		Size: 14.8 KB (14821 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e2578c673d8e347750aad6968df9283d0902cf83b36f7f52eaa2c169fde4886c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10409365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21abd46018664ec1d774ed0ccf028420f6687e33f812018fc3a910dc1ce6014`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdc9114678c7494cfff4d6d27e8c14856724b7b46c06d21e6f5309bb10cfd3e`  
		Last Modified: Thu, 14 Aug 2025 18:48:38 GMT  
		Size: 6.3 MB (6277644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9345987e164f0a7a3c9724b12596354d6f5b27a55c274c5943cf749ce9826044`  
		Last Modified: Thu, 14 Aug 2025 18:48:37 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac90761c84b8f60ad18110b9e9ff4b720ab1d809ff03b57faf042e634d59447`  
		Last Modified: Thu, 14 Aug 2025 18:48:38 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5b917f85bbda7141f8205a4c9d33e28145986c0124ea61f249bd1dbddc4eb538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b21a2426a39cfaf66ebf67d14f2866bfd16bf48c2083eed033b2421bd386a90`

```dockerfile
```

-	Layers:
	-	`sha256:e7738d4b72278c061ab6dd0a6f25f99f4c87e2797157b8dac4f79cea46c6760a`  
		Last Modified: Thu, 14 Aug 2025 20:56:49 GMT  
		Size: 14.9 KB (14865 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:30ad03d77dfb5de88442d0f29c490713d82448efd77693faf7b0935a99453b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9985901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23f66326a77590bc41eb0a5f9f97a5c40ca317276be7cdaf7f7322df7416182`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3e45745642d3a22ccb49be50acc20c0214bd2a5273c0975019b6597df4b5d2`  
		Last Modified: Thu, 14 Aug 2025 18:56:45 GMT  
		Size: 6.3 MB (6257816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a20674adfb2e91f75f547789596c957e2840dfa110ac58dcec2f5e6b686fcd`  
		Last Modified: Thu, 14 Aug 2025 18:56:43 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f76e967ee5d9ae2c5527cef9bb9c8edd4f553ba6495330dc86ee3565f14fc6`  
		Last Modified: Thu, 14 Aug 2025 18:56:43 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:050addcc71308640a4197a465ab8b25fd37500d546c2fbade4232636badd6976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44be2d0d1465d7c59fd92abeb1e0ea0dc33b19b0122cfa12d0204c30e4d4ae13`

```dockerfile
```

-	Layers:
	-	`sha256:66f52a56e2b84f4136709b50caf6b3e34917205c3aeba573456e28d55213cdaa`  
		Last Modified: Thu, 14 Aug 2025 20:56:52 GMT  
		Size: 14.8 KB (14781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine` - linux; s390x

```console
$ docker pull nats@sha256:2bf7f126291a09aa21ef2c65fc041fedfe9e9e29e16a8858bf193280e1318fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10271313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e03788a43a2cfeaefbb6d84b08849b6b847b39eeab7af6cfa746c5475cc49a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813401984db76a6756e0db9016fe48ee5c9d82865d147dd243a26b51b2aad684`  
		Last Modified: Thu, 14 Aug 2025 18:35:37 GMT  
		Size: 6.6 MB (6625370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968c785997911db8d7fa72cfc92186b2fc98d2dd5485d575df8bede6c19e3837`  
		Last Modified: Thu, 14 Aug 2025 18:35:38 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5213bbb60ea3349a52da162a1ed048b3650fabc2973bb84980b33601e46410af`  
		Last Modified: Thu, 14 Aug 2025 18:35:37 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:068c939c8d89bfd8a734c0c4fcb03e2f6122fb7cb278e2af5857d850feb3c05c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f0a7a9a995483ed6030887daaf0da034c453fa869bd81b7cb6c7e352c4e8daa`

```dockerfile
```

-	Layers:
	-	`sha256:4f8fbf204f658abfd1d495febd491047b4ab613c794be7a1f20e98c98ef2c224`  
		Last Modified: Thu, 14 Aug 2025 20:56:55 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-alpine3.22`

```console
$ docker pull nats@sha256:71092f77d707a4a81b12aca5096d6b2d2e07ad16aa57c84066940a17af74f61a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.11-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:9e5633ac7584fc4e80d34be3ff7e15aa3fabec79a5573c2d9abefcf1f7761d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10586751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dfa54630538e8565a0953e5d7316c4b92bd17e293ec333e94f52be2094e7300`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ab6e8880f219a2dd7752796195d9939c137da1ea12c10015c60812ca497573`  
		Last Modified: Thu, 14 Aug 2025 17:21:49 GMT  
		Size: 6.8 MB (6786090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283833608b5ae7ddb376c701f296ad922908c7627de5632ba6e83601e7ac8355`  
		Last Modified: Thu, 14 Aug 2025 17:21:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3411c495c894b3b46ad114eceb39fb6deff204dacab199804c51fd2e1a33a5ae`  
		Last Modified: Thu, 14 Aug 2025 17:21:49 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:d90e427f49684d9b241e599c42a542365675aa62dd6d92a617694d503903cfcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299652c57abf36d15568386e529c8a81ada9d5600ced03a88bccc20b7a50be31`

```dockerfile
```

-	Layers:
	-	`sha256:4ff271d6ce9dacd8101fce3d16eda36e2bbe12422efe9c37df07a8f681004669`  
		Last Modified: Thu, 14 Aug 2025 17:56:25 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:2cfaa354cfe1d863108af5b170d266f632b75f3785be68158e9e0cd1170c640a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10004611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:decbc388e2e168ea436dfa71f5e8cac800997860eb2b021cab4f5e4eec76027f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381ebd5419e3fec8229c2bc4e50847a161b2d4865cfcb4e6733a0ea3c32c77b4`  
		Last Modified: Thu, 14 Aug 2025 18:30:15 GMT  
		Size: 6.5 MB (6502730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37fce2ec2d65289a1c9ac7f39b6ae87b35135e3b107484e7e844793f8d7ff565`  
		Last Modified: Thu, 14 Aug 2025 17:37:15 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872252a349b6a653af65ab2ffc9f0d3cf5eeca6d0e42153f5c303d068d5e1812`  
		Last Modified: Thu, 14 Aug 2025 17:37:18 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:14ef749c437d808301a1efe45e399507ff98890b94c616d0007f1534cc8ab482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac20fd9b620208d75d0fd87edc4b9f19c291e788b7e21cc16cbdb65e53dac741`

```dockerfile
```

-	Layers:
	-	`sha256:57504cb714044ba92951c29c12ec66ede4547725749d0a068268c4cb751a035d`  
		Last Modified: Thu, 14 Aug 2025 20:56:44 GMT  
		Size: 14.8 KB (14821 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:1dc6b44e4b33dbe327dda601fff6bb363ef44c34a4ab2177f307f2d9937f49a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9712521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8885fe376c67ec4357739c5950356acebf63efd04e908fdd24e82f77fbfc7511`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b47ccb42d9de5fae140120c5d63f9ac56f0c1a50c858bfdb2926a8b8c9fa01`  
		Last Modified: Thu, 14 Aug 2025 17:20:49 GMT  
		Size: 6.5 MB (6492514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ae165d2cd161f3b90c15a6ebf63ef30cd24b1314b6c1c9ccfdfe1929e38949`  
		Last Modified: Thu, 14 Aug 2025 17:20:49 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0ad244a682bc355346daaf39628ff905c5a9830e058a1e989c513f9abf0f34`  
		Last Modified: Thu, 14 Aug 2025 17:20:49 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:f63e9df6411bb2032dedb0fe108e98c278fa2dc1239ac4181f3aefe3dc522497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e855d196a62bbe9f94bd2c44e04b0d5cacb3afdcd63e28f775fa65001122f6a0`

```dockerfile
```

-	Layers:
	-	`sha256:d69e84adacba24383fb74725a58e3be312fd8246fa5942fd3aa8c1b8b60cc567`  
		Last Modified: Thu, 14 Aug 2025 17:56:31 GMT  
		Size: 14.8 KB (14821 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e2578c673d8e347750aad6968df9283d0902cf83b36f7f52eaa2c169fde4886c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10409365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21abd46018664ec1d774ed0ccf028420f6687e33f812018fc3a910dc1ce6014`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdc9114678c7494cfff4d6d27e8c14856724b7b46c06d21e6f5309bb10cfd3e`  
		Last Modified: Thu, 14 Aug 2025 18:48:38 GMT  
		Size: 6.3 MB (6277644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9345987e164f0a7a3c9724b12596354d6f5b27a55c274c5943cf749ce9826044`  
		Last Modified: Thu, 14 Aug 2025 18:48:37 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac90761c84b8f60ad18110b9e9ff4b720ab1d809ff03b57faf042e634d59447`  
		Last Modified: Thu, 14 Aug 2025 18:48:38 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5b917f85bbda7141f8205a4c9d33e28145986c0124ea61f249bd1dbddc4eb538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b21a2426a39cfaf66ebf67d14f2866bfd16bf48c2083eed033b2421bd386a90`

```dockerfile
```

-	Layers:
	-	`sha256:e7738d4b72278c061ab6dd0a6f25f99f4c87e2797157b8dac4f79cea46c6760a`  
		Last Modified: Thu, 14 Aug 2025 20:56:49 GMT  
		Size: 14.9 KB (14865 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:30ad03d77dfb5de88442d0f29c490713d82448efd77693faf7b0935a99453b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9985901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23f66326a77590bc41eb0a5f9f97a5c40ca317276be7cdaf7f7322df7416182`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3e45745642d3a22ccb49be50acc20c0214bd2a5273c0975019b6597df4b5d2`  
		Last Modified: Thu, 14 Aug 2025 18:56:45 GMT  
		Size: 6.3 MB (6257816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a20674adfb2e91f75f547789596c957e2840dfa110ac58dcec2f5e6b686fcd`  
		Last Modified: Thu, 14 Aug 2025 18:56:43 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f76e967ee5d9ae2c5527cef9bb9c8edd4f553ba6495330dc86ee3565f14fc6`  
		Last Modified: Thu, 14 Aug 2025 18:56:43 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:050addcc71308640a4197a465ab8b25fd37500d546c2fbade4232636badd6976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44be2d0d1465d7c59fd92abeb1e0ea0dc33b19b0122cfa12d0204c30e4d4ae13`

```dockerfile
```

-	Layers:
	-	`sha256:66f52a56e2b84f4136709b50caf6b3e34917205c3aeba573456e28d55213cdaa`  
		Last Modified: Thu, 14 Aug 2025 20:56:52 GMT  
		Size: 14.8 KB (14781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:2bf7f126291a09aa21ef2c65fc041fedfe9e9e29e16a8858bf193280e1318fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10271313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e03788a43a2cfeaefbb6d84b08849b6b847b39eeab7af6cfa746c5475cc49a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813401984db76a6756e0db9016fe48ee5c9d82865d147dd243a26b51b2aad684`  
		Last Modified: Thu, 14 Aug 2025 18:35:37 GMT  
		Size: 6.6 MB (6625370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968c785997911db8d7fa72cfc92186b2fc98d2dd5485d575df8bede6c19e3837`  
		Last Modified: Thu, 14 Aug 2025 18:35:38 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5213bbb60ea3349a52da162a1ed048b3650fabc2973bb84980b33601e46410af`  
		Last Modified: Thu, 14 Aug 2025 18:35:37 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:068c939c8d89bfd8a734c0c4fcb03e2f6122fb7cb278e2af5857d850feb3c05c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f0a7a9a995483ed6030887daaf0da034c453fa869bd81b7cb6c7e352c4e8daa`

```dockerfile
```

-	Layers:
	-	`sha256:4f8fbf204f658abfd1d495febd491047b4ab613c794be7a1f20e98c98ef2c224`  
		Last Modified: Thu, 14 Aug 2025 20:56:55 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-linux`

```console
$ docker pull nats@sha256:afa7b504a629a7e9f8b4a3984a4dd796fe58a5267adbe0c18af723277657af7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.11-linux` - linux; amd64

```console
$ docker pull nats@sha256:5634002bb5af84b0379f0de363bf0027b76bd6cf1a1db66ad254ae945a163cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6340078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d63b90f51c086da0db2adbc1a2ad7102ecabb8fa67c2470fdc2217b40a4d922`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b663fe8cd396789f2474139e39527f819c3a482db5e25e230cacaadd75df18ce`  
		Last Modified: Thu, 14 Aug 2025 17:27:46 GMT  
		Size: 6.3 MB (6339570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e38b65a6463af6a5ebdc0b02115f51a91399b2710a2758586bbeda7b6d50ba`  
		Last Modified: Thu, 14 Aug 2025 17:27:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:2ab05007143b6795815ff8714f15842e070df35013849973ca0b2f3552177ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310bb9bbe1f9febd06c494bb2dd5b961d7bf71acc8bf0b2fb53e0834a8cc2117`

```dockerfile
```

-	Layers:
	-	`sha256:85acdef1c273fe4667fee682e56c38f81137085631f156c2949814b3bc0d0bee`  
		Last Modified: Thu, 14 Aug 2025 20:56:26 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:40d95d59739fe46433103f4d262d1dd789f75ee44e99c640ea6457cf05487501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6054066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492743618ce250d8b5f53bf5f1e12404d57c3ec44625d5b44726e86f9bba5086`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f10f27efc9fb4dc2b4cdaada3f99aa2ffb9ebc99496fd55f1920263e51b914c9`  
		Last Modified: Thu, 14 Aug 2025 18:07:33 GMT  
		Size: 6.1 MB (6053556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bdfede140a8dbbb6956c184b88de98cc1662ecbef253a2a4433bc47021d07dc`  
		Last Modified: Thu, 14 Aug 2025 18:07:33 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:06dde395a53d1e08b8fd585a2037a3d0579d0cf26446b77df720fb5c757064f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b6f621ca40cc0a37945b871d68296b32cdb51732868485359bc907292b6eba`

```dockerfile
```

-	Layers:
	-	`sha256:6cffdd7549f5659166afe24fb85e23cfebf2409e108e1f347151569e8e28ba38`  
		Last Modified: Thu, 14 Aug 2025 20:56:30 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:815e928020aef447482878a6cef15fd72ac0f9d767b8309b032f7fb8feb7a353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6043424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbbf5945fb4360c4f621c54027b1cb47034cc2fa4d455ccc3f90923c1fe13761`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ba52e77e96ac90555714325e16a7b63d377c42dbeec68ba24cd503063cf7b9e0`  
		Last Modified: Thu, 14 Aug 2025 17:27:10 GMT  
		Size: 6.0 MB (6042914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ee5e05524b58d5802a62546f6f2347446d5321c4e8d583722db5b777d831d1`  
		Last Modified: Thu, 14 Aug 2025 17:27:08 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:842f4f4569460f34fc562978f687fc36581c388b02ab14cdad623893d588f5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2b1c717567f7faa2dde66fcb89acd6dcf382ec81408e1c26ecb2d68f03d105`

```dockerfile
```

-	Layers:
	-	`sha256:62da1307e4b0132c952bdd53d1b82eb3e96fa2934b1b582a8b7277351ddc31cd`  
		Last Modified: Thu, 14 Aug 2025 20:56:33 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d46af1d33927787659e676ea4714a6d53c8ba71956e0cda595d30ab277af5341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b7bb1d1d30e4a8233087664e0b5540f3e42f49f27589cfb43d23bacbeb63ffe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5823b59d47a0c660012e09655022b6660ce21c617ee2978f3edacb2ac344cb9f`  
		Last Modified: Thu, 14 Aug 2025 19:46:02 GMT  
		Size: 5.8 MB (5827281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e915dc222e2df5e58849a12f73e5fcede2bc08f2c98fd12f234ad34883849b`  
		Last Modified: Thu, 14 Aug 2025 19:46:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:4e9ff58758ddaea565568a15d4d049d69f51f01f69e9e0e517c68718dfe93ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a92dc3160475131a9aa4330ac0e14dedb97f5d4d57d5a386b4b1033afe203bc`

```dockerfile
```

-	Layers:
	-	`sha256:efd6b414c46e44a7c6cd8407e5887b4066f7e91785d16647bdfc24cb7dfb35a4`  
		Last Modified: Thu, 14 Aug 2025 20:56:36 GMT  
		Size: 10.6 KB (10649 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:70ad109d17470e9dbefe10df2ea372ea487e5a28cf96934110c5f6e6b118c4ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5807845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcf49d098aee252cf17a17945623b98c12312f01460230bd2494a20949c2703`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:221614c6b4427295323da315f973992219d61abd51aa73f549b80d617ceed783`  
		Last Modified: Thu, 14 Aug 2025 20:45:44 GMT  
		Size: 5.8 MB (5807337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea070ca5e9aa9e1edaa1764d931a0b0e385793e5b3124004b4ba91da5efc9e9`  
		Last Modified: Thu, 14 Aug 2025 20:45:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:bf4cec841a590e736bc48410cd41b4eb5176b07e39b161d5827a0dfe411fb72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd14ce8eff83929fceb915b93bd248d9837b402d7c289ab095bb35b5306608d`

```dockerfile
```

-	Layers:
	-	`sha256:f968b5bb7ad9cd95b31e5948c6d247e8ff2820fa830ca084746ac40f662b15d1`  
		Last Modified: Thu, 14 Aug 2025 23:56:26 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-linux` - linux; s390x

```console
$ docker pull nats@sha256:66e24c97e22fd4db570efbde5c154dad761a934509688d1066ff6faf16c6ff8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6173621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5239fb0f4852c75ada10240d6ad54ccabbe1c300c54385271ab0d9c9a16d599`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 Aug 2025 12:51:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 Aug 2025 12:51:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 Aug 2025 12:51:02 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 Aug 2025 12:51:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 Aug 2025 12:51:02 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 Aug 2025 12:51:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:84a200250dfb971cfcf23197670e7ccfcfae55787bc8842c737081462376b978`  
		Last Modified: Mon, 04 Aug 2025 18:10:15 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5013d749e0797d9a012b7f969383e42b359cae57b7b1945f62eae07e6f12bbb`  
		Last Modified: Mon, 04 Aug 2025 18:10:15 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-linux` - unknown; unknown

```console
$ docker pull nats@sha256:3e90c2e5acc844d0189d6d664df76b3fc55d6438e1be7c1146763d00098ed8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469d8c0a969e19358745ad9513225279dd13b3d004003729b94ccd524773ffb5`

```dockerfile
```

-	Layers:
	-	`sha256:3490df75b7ac2f5425cf2a5decc578d60f595e9e0317faa4e73c20548b16f138`  
		Last Modified: Mon, 04 Aug 2025 20:56:51 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-nanoserver`

```console
$ docker pull nats@sha256:4b5bc1dda10956fffbd5637c74ca36f1f8e8999841816091381b80f7f4368b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2.11-nanoserver` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:ad9de8f09f3634777b25adb56728db4ae6804eb3e93cf167d338af2569150272
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129178975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3e567374bac2065f94b8560a0f1747b427e881b5faa654919d1f7abccc554d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Thu, 14 Aug 2025 18:14:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 14 Aug 2025 18:14:05 GMT
RUN cmd /S /C #(nop) COPY file:3fa3039439cf4074860757aeaaa6c458fcb2a8fd53320637e2edb93570462bde in C:\nats-server.exe 
# Thu, 14 Aug 2025 18:14:06 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Aug 2025 18:14:07 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 14 Aug 2025 18:14:08 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Aug 2025 18:14:09 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70dd762bbc2519848d92e4250ffd2e8ad506e67e2ccc6edb8b28deb7bd6a4cc3`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8303cc1b67f588378cd15d48f0f9092ea5f9e1d8e2832d99a509bdd9c8ff70a`  
		Last Modified: Thu, 14 Aug 2025 18:14:54 GMT  
		Size: 6.5 MB (6512850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5204fc3573607851e777581d8f3393c06877a1b385138e9ddb562e41c44ae04f`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5811e67cadd8e8c18aa9f537c4147610482318cb56ca5e6a1ff3cff5d96e4cfc`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b880e68edcdaf39200bd33cc61fd60fab56c1eae85a872652a20730da3d12a`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbef80910535149a3762e6bfc014c51084a8c11fa366889b246185411c39fb9`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:4b5bc1dda10956fffbd5637c74ca36f1f8e8999841816091381b80f7f4368b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:ad9de8f09f3634777b25adb56728db4ae6804eb3e93cf167d338af2569150272
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129178975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3e567374bac2065f94b8560a0f1747b427e881b5faa654919d1f7abccc554d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Thu, 14 Aug 2025 18:14:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 14 Aug 2025 18:14:05 GMT
RUN cmd /S /C #(nop) COPY file:3fa3039439cf4074860757aeaaa6c458fcb2a8fd53320637e2edb93570462bde in C:\nats-server.exe 
# Thu, 14 Aug 2025 18:14:06 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Aug 2025 18:14:07 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 14 Aug 2025 18:14:08 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Aug 2025 18:14:09 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70dd762bbc2519848d92e4250ffd2e8ad506e67e2ccc6edb8b28deb7bd6a4cc3`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8303cc1b67f588378cd15d48f0f9092ea5f9e1d8e2832d99a509bdd9c8ff70a`  
		Last Modified: Thu, 14 Aug 2025 18:14:54 GMT  
		Size: 6.5 MB (6512850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5204fc3573607851e777581d8f3393c06877a1b385138e9ddb562e41c44ae04f`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5811e67cadd8e8c18aa9f537c4147610482318cb56ca5e6a1ff3cff5d96e4cfc`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b880e68edcdaf39200bd33cc61fd60fab56c1eae85a872652a20730da3d12a`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbef80910535149a3762e6bfc014c51084a8c11fa366889b246185411c39fb9`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-scratch`

```console
$ docker pull nats@sha256:afa7b504a629a7e9f8b4a3984a4dd796fe58a5267adbe0c18af723277657af7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.11-scratch` - linux; amd64

```console
$ docker pull nats@sha256:5634002bb5af84b0379f0de363bf0027b76bd6cf1a1db66ad254ae945a163cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6340078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d63b90f51c086da0db2adbc1a2ad7102ecabb8fa67c2470fdc2217b40a4d922`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b663fe8cd396789f2474139e39527f819c3a482db5e25e230cacaadd75df18ce`  
		Last Modified: Thu, 14 Aug 2025 17:27:46 GMT  
		Size: 6.3 MB (6339570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e38b65a6463af6a5ebdc0b02115f51a91399b2710a2758586bbeda7b6d50ba`  
		Last Modified: Thu, 14 Aug 2025 17:27:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:2ab05007143b6795815ff8714f15842e070df35013849973ca0b2f3552177ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310bb9bbe1f9febd06c494bb2dd5b961d7bf71acc8bf0b2fb53e0834a8cc2117`

```dockerfile
```

-	Layers:
	-	`sha256:85acdef1c273fe4667fee682e56c38f81137085631f156c2949814b3bc0d0bee`  
		Last Modified: Thu, 14 Aug 2025 20:56:26 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:40d95d59739fe46433103f4d262d1dd789f75ee44e99c640ea6457cf05487501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6054066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492743618ce250d8b5f53bf5f1e12404d57c3ec44625d5b44726e86f9bba5086`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f10f27efc9fb4dc2b4cdaada3f99aa2ffb9ebc99496fd55f1920263e51b914c9`  
		Last Modified: Thu, 14 Aug 2025 18:07:33 GMT  
		Size: 6.1 MB (6053556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bdfede140a8dbbb6956c184b88de98cc1662ecbef253a2a4433bc47021d07dc`  
		Last Modified: Thu, 14 Aug 2025 18:07:33 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:06dde395a53d1e08b8fd585a2037a3d0579d0cf26446b77df720fb5c757064f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b6f621ca40cc0a37945b871d68296b32cdb51732868485359bc907292b6eba`

```dockerfile
```

-	Layers:
	-	`sha256:6cffdd7549f5659166afe24fb85e23cfebf2409e108e1f347151569e8e28ba38`  
		Last Modified: Thu, 14 Aug 2025 20:56:30 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:815e928020aef447482878a6cef15fd72ac0f9d767b8309b032f7fb8feb7a353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6043424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbbf5945fb4360c4f621c54027b1cb47034cc2fa4d455ccc3f90923c1fe13761`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ba52e77e96ac90555714325e16a7b63d377c42dbeec68ba24cd503063cf7b9e0`  
		Last Modified: Thu, 14 Aug 2025 17:27:10 GMT  
		Size: 6.0 MB (6042914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ee5e05524b58d5802a62546f6f2347446d5321c4e8d583722db5b777d831d1`  
		Last Modified: Thu, 14 Aug 2025 17:27:08 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:842f4f4569460f34fc562978f687fc36581c388b02ab14cdad623893d588f5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2b1c717567f7faa2dde66fcb89acd6dcf382ec81408e1c26ecb2d68f03d105`

```dockerfile
```

-	Layers:
	-	`sha256:62da1307e4b0132c952bdd53d1b82eb3e96fa2934b1b582a8b7277351ddc31cd`  
		Last Modified: Thu, 14 Aug 2025 20:56:33 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d46af1d33927787659e676ea4714a6d53c8ba71956e0cda595d30ab277af5341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b7bb1d1d30e4a8233087664e0b5540f3e42f49f27589cfb43d23bacbeb63ffe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5823b59d47a0c660012e09655022b6660ce21c617ee2978f3edacb2ac344cb9f`  
		Last Modified: Thu, 14 Aug 2025 19:46:02 GMT  
		Size: 5.8 MB (5827281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e915dc222e2df5e58849a12f73e5fcede2bc08f2c98fd12f234ad34883849b`  
		Last Modified: Thu, 14 Aug 2025 19:46:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4e9ff58758ddaea565568a15d4d049d69f51f01f69e9e0e517c68718dfe93ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a92dc3160475131a9aa4330ac0e14dedb97f5d4d57d5a386b4b1033afe203bc`

```dockerfile
```

-	Layers:
	-	`sha256:efd6b414c46e44a7c6cd8407e5887b4066f7e91785d16647bdfc24cb7dfb35a4`  
		Last Modified: Thu, 14 Aug 2025 20:56:36 GMT  
		Size: 10.6 KB (10649 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:70ad109d17470e9dbefe10df2ea372ea487e5a28cf96934110c5f6e6b118c4ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5807845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcf49d098aee252cf17a17945623b98c12312f01460230bd2494a20949c2703`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:221614c6b4427295323da315f973992219d61abd51aa73f549b80d617ceed783`  
		Last Modified: Thu, 14 Aug 2025 20:45:44 GMT  
		Size: 5.8 MB (5807337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea070ca5e9aa9e1edaa1764d931a0b0e385793e5b3124004b4ba91da5efc9e9`  
		Last Modified: Thu, 14 Aug 2025 20:45:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:bf4cec841a590e736bc48410cd41b4eb5176b07e39b161d5827a0dfe411fb72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd14ce8eff83929fceb915b93bd248d9837b402d7c289ab095bb35b5306608d`

```dockerfile
```

-	Layers:
	-	`sha256:f968b5bb7ad9cd95b31e5948c6d247e8ff2820fa830ca084746ac40f662b15d1`  
		Last Modified: Thu, 14 Aug 2025 23:56:26 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11-scratch` - linux; s390x

```console
$ docker pull nats@sha256:66e24c97e22fd4db570efbde5c154dad761a934509688d1066ff6faf16c6ff8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6173621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5239fb0f4852c75ada10240d6ad54ccabbe1c300c54385271ab0d9c9a16d599`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 Aug 2025 12:51:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 Aug 2025 12:51:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 Aug 2025 12:51:02 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 Aug 2025 12:51:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 Aug 2025 12:51:02 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 Aug 2025 12:51:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:84a200250dfb971cfcf23197670e7ccfcfae55787bc8842c737081462376b978`  
		Last Modified: Mon, 04 Aug 2025 18:10:15 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5013d749e0797d9a012b7f969383e42b359cae57b7b1945f62eae07e6f12bbb`  
		Last Modified: Mon, 04 Aug 2025 18:10:15 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:3e90c2e5acc844d0189d6d664df76b3fc55d6438e1be7c1146763d00098ed8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469d8c0a969e19358745ad9513225279dd13b3d004003729b94ccd524773ffb5`

```dockerfile
```

-	Layers:
	-	`sha256:3490df75b7ac2f5425cf2a5decc578d60f595e9e0317faa4e73c20548b16f138`  
		Last Modified: Mon, 04 Aug 2025 20:56:51 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11-windowsservercore`

```console
$ docker pull nats@sha256:cd40ad4037d8bcb19778d0ec3407978059ea88d895747dfce3ea1be3f83f5760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2.11-windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:ff0d0047ceb610a0b73edcb6d12305bdf06e08a127258cf923e1aec9645ec419
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2288892735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe5b93e3cd45a63955014ff0d53cf5383f91b868d6bacf1c242ce4861d0a3fe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Thu, 14 Aug 2025 17:24:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 14 Aug 2025 17:24:18 GMT
ENV NATS_DOCKERIZED=1
# Thu, 14 Aug 2025 17:24:19 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 17:24:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.8/nats-server-v2.11.8-windows-amd64.zip
# Thu, 14 Aug 2025 17:24:21 GMT
ENV NATS_SERVER_SHASUM=3dd98465626e8c6ed92a784ef13c3f956c7e87fbbb4ee86cc198e377565eaeaf
# Thu, 14 Aug 2025 17:24:28 GMT
RUN Set-PSDebug -Trace 2
# Thu, 14 Aug 2025 17:24:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 14 Aug 2025 17:24:44 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Aug 2025 17:24:45 GMT
EXPOSE 4222 6222 8222
# Thu, 14 Aug 2025 17:24:46 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Aug 2025 17:24:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3f006d1cb294833347c0dcdeff82dda52af9acbea696337fd8408869317713`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e0fe1f9e451f5b78de6f2eabbcf9dd583e44cc8efca284c024e6fc31fea206`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4c9efb293cf4538944d58d49d978df5a06ed2586f43c0312291c6ed0854b98`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4fcdec518a7d5e9cbdbb2398711d526df04c6abd46f6dc74c91ce20cb62a28`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f32d8dbe729b86cde1eafd2da61359f32dab9aa4ff767aa70b3dc9351ba01c3`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1453289e44dd8e7a29b2a8395640bb6a2e2ebd47060a6bfe129031ce2072d7`  
		Last Modified: Thu, 14 Aug 2025 17:26:08 GMT  
		Size: 336.2 KB (336246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db38558f3d85860c055f99e79e865d42a17dd691a4f83ea93e0f8a5e391d125`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 6.9 MB (6852407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb87097b18d82c7dc42b80c5f6912e34cd08ecb316ffd445266fbb02ee18352b`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828b5772011538e3bb3bd9055b2b9e9b10bb6ffd46dc54a1d765d3e2dcfb03a6`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd3abb758a5b3c339001a04d7364df2b54b00e27711aecf5f44a76323ef676f`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366367ce039c79734b9ad15e13867ea0fd5f18ee46cc185dde59b3507a9b3392`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:cd40ad4037d8bcb19778d0ec3407978059ea88d895747dfce3ea1be3f83f5760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:ff0d0047ceb610a0b73edcb6d12305bdf06e08a127258cf923e1aec9645ec419
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2288892735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe5b93e3cd45a63955014ff0d53cf5383f91b868d6bacf1c242ce4861d0a3fe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Thu, 14 Aug 2025 17:24:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 14 Aug 2025 17:24:18 GMT
ENV NATS_DOCKERIZED=1
# Thu, 14 Aug 2025 17:24:19 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 17:24:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.8/nats-server-v2.11.8-windows-amd64.zip
# Thu, 14 Aug 2025 17:24:21 GMT
ENV NATS_SERVER_SHASUM=3dd98465626e8c6ed92a784ef13c3f956c7e87fbbb4ee86cc198e377565eaeaf
# Thu, 14 Aug 2025 17:24:28 GMT
RUN Set-PSDebug -Trace 2
# Thu, 14 Aug 2025 17:24:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 14 Aug 2025 17:24:44 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Aug 2025 17:24:45 GMT
EXPOSE 4222 6222 8222
# Thu, 14 Aug 2025 17:24:46 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Aug 2025 17:24:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3f006d1cb294833347c0dcdeff82dda52af9acbea696337fd8408869317713`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e0fe1f9e451f5b78de6f2eabbcf9dd583e44cc8efca284c024e6fc31fea206`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4c9efb293cf4538944d58d49d978df5a06ed2586f43c0312291c6ed0854b98`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4fcdec518a7d5e9cbdbb2398711d526df04c6abd46f6dc74c91ce20cb62a28`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f32d8dbe729b86cde1eafd2da61359f32dab9aa4ff767aa70b3dc9351ba01c3`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1453289e44dd8e7a29b2a8395640bb6a2e2ebd47060a6bfe129031ce2072d7`  
		Last Modified: Thu, 14 Aug 2025 17:26:08 GMT  
		Size: 336.2 KB (336246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db38558f3d85860c055f99e79e865d42a17dd691a4f83ea93e0f8a5e391d125`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 6.9 MB (6852407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb87097b18d82c7dc42b80c5f6912e34cd08ecb316ffd445266fbb02ee18352b`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828b5772011538e3bb3bd9055b2b9e9b10bb6ffd46dc54a1d765d3e2dcfb03a6`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd3abb758a5b3c339001a04d7364df2b54b00e27711aecf5f44a76323ef676f`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366367ce039c79734b9ad15e13867ea0fd5f18ee46cc185dde59b3507a9b3392`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.8`

```console
$ docker pull nats@sha256:a5ff047237848e015828249e9cfa14722b43d7f8eebf6067bca826de0694ff68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.20348.4052; amd64

### `nats:2.11.8` - linux; amd64

```console
$ docker pull nats@sha256:5634002bb5af84b0379f0de363bf0027b76bd6cf1a1db66ad254ae945a163cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6340078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d63b90f51c086da0db2adbc1a2ad7102ecabb8fa67c2470fdc2217b40a4d922`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b663fe8cd396789f2474139e39527f819c3a482db5e25e230cacaadd75df18ce`  
		Last Modified: Thu, 14 Aug 2025 17:27:46 GMT  
		Size: 6.3 MB (6339570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e38b65a6463af6a5ebdc0b02115f51a91399b2710a2758586bbeda7b6d50ba`  
		Last Modified: Thu, 14 Aug 2025 17:27:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.8` - unknown; unknown

```console
$ docker pull nats@sha256:2ab05007143b6795815ff8714f15842e070df35013849973ca0b2f3552177ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310bb9bbe1f9febd06c494bb2dd5b961d7bf71acc8bf0b2fb53e0834a8cc2117`

```dockerfile
```

-	Layers:
	-	`sha256:85acdef1c273fe4667fee682e56c38f81137085631f156c2949814b3bc0d0bee`  
		Last Modified: Thu, 14 Aug 2025 20:56:26 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.8` - linux; arm variant v6

```console
$ docker pull nats@sha256:40d95d59739fe46433103f4d262d1dd789f75ee44e99c640ea6457cf05487501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6054066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492743618ce250d8b5f53bf5f1e12404d57c3ec44625d5b44726e86f9bba5086`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f10f27efc9fb4dc2b4cdaada3f99aa2ffb9ebc99496fd55f1920263e51b914c9`  
		Last Modified: Thu, 14 Aug 2025 18:07:33 GMT  
		Size: 6.1 MB (6053556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bdfede140a8dbbb6956c184b88de98cc1662ecbef253a2a4433bc47021d07dc`  
		Last Modified: Thu, 14 Aug 2025 18:07:33 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.8` - unknown; unknown

```console
$ docker pull nats@sha256:06dde395a53d1e08b8fd585a2037a3d0579d0cf26446b77df720fb5c757064f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b6f621ca40cc0a37945b871d68296b32cdb51732868485359bc907292b6eba`

```dockerfile
```

-	Layers:
	-	`sha256:6cffdd7549f5659166afe24fb85e23cfebf2409e108e1f347151569e8e28ba38`  
		Last Modified: Thu, 14 Aug 2025 20:56:30 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.8` - linux; arm variant v7

```console
$ docker pull nats@sha256:815e928020aef447482878a6cef15fd72ac0f9d767b8309b032f7fb8feb7a353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6043424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbbf5945fb4360c4f621c54027b1cb47034cc2fa4d455ccc3f90923c1fe13761`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ba52e77e96ac90555714325e16a7b63d377c42dbeec68ba24cd503063cf7b9e0`  
		Last Modified: Thu, 14 Aug 2025 17:27:10 GMT  
		Size: 6.0 MB (6042914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ee5e05524b58d5802a62546f6f2347446d5321c4e8d583722db5b777d831d1`  
		Last Modified: Thu, 14 Aug 2025 17:27:08 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.8` - unknown; unknown

```console
$ docker pull nats@sha256:842f4f4569460f34fc562978f687fc36581c388b02ab14cdad623893d588f5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2b1c717567f7faa2dde66fcb89acd6dcf382ec81408e1c26ecb2d68f03d105`

```dockerfile
```

-	Layers:
	-	`sha256:62da1307e4b0132c952bdd53d1b82eb3e96fa2934b1b582a8b7277351ddc31cd`  
		Last Modified: Thu, 14 Aug 2025 20:56:33 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.8` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d46af1d33927787659e676ea4714a6d53c8ba71956e0cda595d30ab277af5341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b7bb1d1d30e4a8233087664e0b5540f3e42f49f27589cfb43d23bacbeb63ffe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5823b59d47a0c660012e09655022b6660ce21c617ee2978f3edacb2ac344cb9f`  
		Last Modified: Thu, 14 Aug 2025 19:46:02 GMT  
		Size: 5.8 MB (5827281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e915dc222e2df5e58849a12f73e5fcede2bc08f2c98fd12f234ad34883849b`  
		Last Modified: Thu, 14 Aug 2025 19:46:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.8` - unknown; unknown

```console
$ docker pull nats@sha256:4e9ff58758ddaea565568a15d4d049d69f51f01f69e9e0e517c68718dfe93ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a92dc3160475131a9aa4330ac0e14dedb97f5d4d57d5a386b4b1033afe203bc`

```dockerfile
```

-	Layers:
	-	`sha256:efd6b414c46e44a7c6cd8407e5887b4066f7e91785d16647bdfc24cb7dfb35a4`  
		Last Modified: Thu, 14 Aug 2025 20:56:36 GMT  
		Size: 10.6 KB (10649 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.8` - linux; ppc64le

```console
$ docker pull nats@sha256:70ad109d17470e9dbefe10df2ea372ea487e5a28cf96934110c5f6e6b118c4ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5807845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcf49d098aee252cf17a17945623b98c12312f01460230bd2494a20949c2703`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:221614c6b4427295323da315f973992219d61abd51aa73f549b80d617ceed783`  
		Last Modified: Thu, 14 Aug 2025 20:45:44 GMT  
		Size: 5.8 MB (5807337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea070ca5e9aa9e1edaa1764d931a0b0e385793e5b3124004b4ba91da5efc9e9`  
		Last Modified: Thu, 14 Aug 2025 20:45:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.8` - unknown; unknown

```console
$ docker pull nats@sha256:bf4cec841a590e736bc48410cd41b4eb5176b07e39b161d5827a0dfe411fb72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd14ce8eff83929fceb915b93bd248d9837b402d7c289ab095bb35b5306608d`

```dockerfile
```

-	Layers:
	-	`sha256:f968b5bb7ad9cd95b31e5948c6d247e8ff2820fa830ca084746ac40f662b15d1`  
		Last Modified: Thu, 14 Aug 2025 23:56:26 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.8` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:ad9de8f09f3634777b25adb56728db4ae6804eb3e93cf167d338af2569150272
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129178975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3e567374bac2065f94b8560a0f1747b427e881b5faa654919d1f7abccc554d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Thu, 14 Aug 2025 18:14:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 14 Aug 2025 18:14:05 GMT
RUN cmd /S /C #(nop) COPY file:3fa3039439cf4074860757aeaaa6c458fcb2a8fd53320637e2edb93570462bde in C:\nats-server.exe 
# Thu, 14 Aug 2025 18:14:06 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Aug 2025 18:14:07 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 14 Aug 2025 18:14:08 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Aug 2025 18:14:09 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70dd762bbc2519848d92e4250ffd2e8ad506e67e2ccc6edb8b28deb7bd6a4cc3`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8303cc1b67f588378cd15d48f0f9092ea5f9e1d8e2832d99a509bdd9c8ff70a`  
		Last Modified: Thu, 14 Aug 2025 18:14:54 GMT  
		Size: 6.5 MB (6512850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5204fc3573607851e777581d8f3393c06877a1b385138e9ddb562e41c44ae04f`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5811e67cadd8e8c18aa9f537c4147610482318cb56ca5e6a1ff3cff5d96e4cfc`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b880e68edcdaf39200bd33cc61fd60fab56c1eae85a872652a20730da3d12a`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbef80910535149a3762e6bfc014c51084a8c11fa366889b246185411c39fb9`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.8-alpine`

```console
$ docker pull nats@sha256:71092f77d707a4a81b12aca5096d6b2d2e07ad16aa57c84066940a17af74f61a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.11.8-alpine` - linux; amd64

```console
$ docker pull nats@sha256:9e5633ac7584fc4e80d34be3ff7e15aa3fabec79a5573c2d9abefcf1f7761d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10586751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dfa54630538e8565a0953e5d7316c4b92bd17e293ec333e94f52be2094e7300`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ab6e8880f219a2dd7752796195d9939c137da1ea12c10015c60812ca497573`  
		Last Modified: Thu, 14 Aug 2025 17:21:49 GMT  
		Size: 6.8 MB (6786090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283833608b5ae7ddb376c701f296ad922908c7627de5632ba6e83601e7ac8355`  
		Last Modified: Thu, 14 Aug 2025 17:21:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3411c495c894b3b46ad114eceb39fb6deff204dacab199804c51fd2e1a33a5ae`  
		Last Modified: Thu, 14 Aug 2025 17:21:49 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.8-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d90e427f49684d9b241e599c42a542365675aa62dd6d92a617694d503903cfcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299652c57abf36d15568386e529c8a81ada9d5600ced03a88bccc20b7a50be31`

```dockerfile
```

-	Layers:
	-	`sha256:4ff271d6ce9dacd8101fce3d16eda36e2bbe12422efe9c37df07a8f681004669`  
		Last Modified: Thu, 14 Aug 2025 17:56:25 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.8-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:2cfaa354cfe1d863108af5b170d266f632b75f3785be68158e9e0cd1170c640a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10004611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:decbc388e2e168ea436dfa71f5e8cac800997860eb2b021cab4f5e4eec76027f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381ebd5419e3fec8229c2bc4e50847a161b2d4865cfcb4e6733a0ea3c32c77b4`  
		Last Modified: Thu, 14 Aug 2025 18:30:15 GMT  
		Size: 6.5 MB (6502730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37fce2ec2d65289a1c9ac7f39b6ae87b35135e3b107484e7e844793f8d7ff565`  
		Last Modified: Thu, 14 Aug 2025 17:37:15 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872252a349b6a653af65ab2ffc9f0d3cf5eeca6d0e42153f5c303d068d5e1812`  
		Last Modified: Thu, 14 Aug 2025 17:37:18 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.8-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:14ef749c437d808301a1efe45e399507ff98890b94c616d0007f1534cc8ab482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac20fd9b620208d75d0fd87edc4b9f19c291e788b7e21cc16cbdb65e53dac741`

```dockerfile
```

-	Layers:
	-	`sha256:57504cb714044ba92951c29c12ec66ede4547725749d0a068268c4cb751a035d`  
		Last Modified: Thu, 14 Aug 2025 20:56:44 GMT  
		Size: 14.8 KB (14821 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.8-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:1dc6b44e4b33dbe327dda601fff6bb363ef44c34a4ab2177f307f2d9937f49a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9712521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8885fe376c67ec4357739c5950356acebf63efd04e908fdd24e82f77fbfc7511`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b47ccb42d9de5fae140120c5d63f9ac56f0c1a50c858bfdb2926a8b8c9fa01`  
		Last Modified: Thu, 14 Aug 2025 17:20:49 GMT  
		Size: 6.5 MB (6492514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ae165d2cd161f3b90c15a6ebf63ef30cd24b1314b6c1c9ccfdfe1929e38949`  
		Last Modified: Thu, 14 Aug 2025 17:20:49 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0ad244a682bc355346daaf39628ff905c5a9830e058a1e989c513f9abf0f34`  
		Last Modified: Thu, 14 Aug 2025 17:20:49 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.8-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f63e9df6411bb2032dedb0fe108e98c278fa2dc1239ac4181f3aefe3dc522497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e855d196a62bbe9f94bd2c44e04b0d5cacb3afdcd63e28f775fa65001122f6a0`

```dockerfile
```

-	Layers:
	-	`sha256:d69e84adacba24383fb74725a58e3be312fd8246fa5942fd3aa8c1b8b60cc567`  
		Last Modified: Thu, 14 Aug 2025 17:56:31 GMT  
		Size: 14.8 KB (14821 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.8-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e2578c673d8e347750aad6968df9283d0902cf83b36f7f52eaa2c169fde4886c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10409365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21abd46018664ec1d774ed0ccf028420f6687e33f812018fc3a910dc1ce6014`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdc9114678c7494cfff4d6d27e8c14856724b7b46c06d21e6f5309bb10cfd3e`  
		Last Modified: Thu, 14 Aug 2025 18:48:38 GMT  
		Size: 6.3 MB (6277644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9345987e164f0a7a3c9724b12596354d6f5b27a55c274c5943cf749ce9826044`  
		Last Modified: Thu, 14 Aug 2025 18:48:37 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac90761c84b8f60ad18110b9e9ff4b720ab1d809ff03b57faf042e634d59447`  
		Last Modified: Thu, 14 Aug 2025 18:48:38 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.8-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5b917f85bbda7141f8205a4c9d33e28145986c0124ea61f249bd1dbddc4eb538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b21a2426a39cfaf66ebf67d14f2866bfd16bf48c2083eed033b2421bd386a90`

```dockerfile
```

-	Layers:
	-	`sha256:e7738d4b72278c061ab6dd0a6f25f99f4c87e2797157b8dac4f79cea46c6760a`  
		Last Modified: Thu, 14 Aug 2025 20:56:49 GMT  
		Size: 14.9 KB (14865 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.8-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:30ad03d77dfb5de88442d0f29c490713d82448efd77693faf7b0935a99453b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9985901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23f66326a77590bc41eb0a5f9f97a5c40ca317276be7cdaf7f7322df7416182`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3e45745642d3a22ccb49be50acc20c0214bd2a5273c0975019b6597df4b5d2`  
		Last Modified: Thu, 14 Aug 2025 18:56:45 GMT  
		Size: 6.3 MB (6257816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a20674adfb2e91f75f547789596c957e2840dfa110ac58dcec2f5e6b686fcd`  
		Last Modified: Thu, 14 Aug 2025 18:56:43 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f76e967ee5d9ae2c5527cef9bb9c8edd4f553ba6495330dc86ee3565f14fc6`  
		Last Modified: Thu, 14 Aug 2025 18:56:43 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.8-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:050addcc71308640a4197a465ab8b25fd37500d546c2fbade4232636badd6976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44be2d0d1465d7c59fd92abeb1e0ea0dc33b19b0122cfa12d0204c30e4d4ae13`

```dockerfile
```

-	Layers:
	-	`sha256:66f52a56e2b84f4136709b50caf6b3e34917205c3aeba573456e28d55213cdaa`  
		Last Modified: Thu, 14 Aug 2025 20:56:52 GMT  
		Size: 14.8 KB (14781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.8-alpine` - linux; s390x

```console
$ docker pull nats@sha256:2bf7f126291a09aa21ef2c65fc041fedfe9e9e29e16a8858bf193280e1318fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10271313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e03788a43a2cfeaefbb6d84b08849b6b847b39eeab7af6cfa746c5475cc49a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813401984db76a6756e0db9016fe48ee5c9d82865d147dd243a26b51b2aad684`  
		Last Modified: Thu, 14 Aug 2025 18:35:37 GMT  
		Size: 6.6 MB (6625370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968c785997911db8d7fa72cfc92186b2fc98d2dd5485d575df8bede6c19e3837`  
		Last Modified: Thu, 14 Aug 2025 18:35:38 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5213bbb60ea3349a52da162a1ed048b3650fabc2973bb84980b33601e46410af`  
		Last Modified: Thu, 14 Aug 2025 18:35:37 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.8-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:068c939c8d89bfd8a734c0c4fcb03e2f6122fb7cb278e2af5857d850feb3c05c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f0a7a9a995483ed6030887daaf0da034c453fa869bd81b7cb6c7e352c4e8daa`

```dockerfile
```

-	Layers:
	-	`sha256:4f8fbf204f658abfd1d495febd491047b4ab613c794be7a1f20e98c98ef2c224`  
		Last Modified: Thu, 14 Aug 2025 20:56:55 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.8-alpine3.22`

```console
$ docker pull nats@sha256:71092f77d707a4a81b12aca5096d6b2d2e07ad16aa57c84066940a17af74f61a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2.11.8-alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:9e5633ac7584fc4e80d34be3ff7e15aa3fabec79a5573c2d9abefcf1f7761d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10586751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dfa54630538e8565a0953e5d7316c4b92bd17e293ec333e94f52be2094e7300`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ab6e8880f219a2dd7752796195d9939c137da1ea12c10015c60812ca497573`  
		Last Modified: Thu, 14 Aug 2025 17:21:49 GMT  
		Size: 6.8 MB (6786090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283833608b5ae7ddb376c701f296ad922908c7627de5632ba6e83601e7ac8355`  
		Last Modified: Thu, 14 Aug 2025 17:21:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3411c495c894b3b46ad114eceb39fb6deff204dacab199804c51fd2e1a33a5ae`  
		Last Modified: Thu, 14 Aug 2025 17:21:49 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.8-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:d90e427f49684d9b241e599c42a542365675aa62dd6d92a617694d503903cfcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299652c57abf36d15568386e529c8a81ada9d5600ced03a88bccc20b7a50be31`

```dockerfile
```

-	Layers:
	-	`sha256:4ff271d6ce9dacd8101fce3d16eda36e2bbe12422efe9c37df07a8f681004669`  
		Last Modified: Thu, 14 Aug 2025 17:56:25 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.8-alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:2cfaa354cfe1d863108af5b170d266f632b75f3785be68158e9e0cd1170c640a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10004611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:decbc388e2e168ea436dfa71f5e8cac800997860eb2b021cab4f5e4eec76027f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381ebd5419e3fec8229c2bc4e50847a161b2d4865cfcb4e6733a0ea3c32c77b4`  
		Last Modified: Thu, 14 Aug 2025 18:30:15 GMT  
		Size: 6.5 MB (6502730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37fce2ec2d65289a1c9ac7f39b6ae87b35135e3b107484e7e844793f8d7ff565`  
		Last Modified: Thu, 14 Aug 2025 17:37:15 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872252a349b6a653af65ab2ffc9f0d3cf5eeca6d0e42153f5c303d068d5e1812`  
		Last Modified: Thu, 14 Aug 2025 17:37:18 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.8-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:14ef749c437d808301a1efe45e399507ff98890b94c616d0007f1534cc8ab482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac20fd9b620208d75d0fd87edc4b9f19c291e788b7e21cc16cbdb65e53dac741`

```dockerfile
```

-	Layers:
	-	`sha256:57504cb714044ba92951c29c12ec66ede4547725749d0a068268c4cb751a035d`  
		Last Modified: Thu, 14 Aug 2025 20:56:44 GMT  
		Size: 14.8 KB (14821 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.8-alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:1dc6b44e4b33dbe327dda601fff6bb363ef44c34a4ab2177f307f2d9937f49a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9712521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8885fe376c67ec4357739c5950356acebf63efd04e908fdd24e82f77fbfc7511`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b47ccb42d9de5fae140120c5d63f9ac56f0c1a50c858bfdb2926a8b8c9fa01`  
		Last Modified: Thu, 14 Aug 2025 17:20:49 GMT  
		Size: 6.5 MB (6492514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ae165d2cd161f3b90c15a6ebf63ef30cd24b1314b6c1c9ccfdfe1929e38949`  
		Last Modified: Thu, 14 Aug 2025 17:20:49 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0ad244a682bc355346daaf39628ff905c5a9830e058a1e989c513f9abf0f34`  
		Last Modified: Thu, 14 Aug 2025 17:20:49 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.8-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:f63e9df6411bb2032dedb0fe108e98c278fa2dc1239ac4181f3aefe3dc522497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e855d196a62bbe9f94bd2c44e04b0d5cacb3afdcd63e28f775fa65001122f6a0`

```dockerfile
```

-	Layers:
	-	`sha256:d69e84adacba24383fb74725a58e3be312fd8246fa5942fd3aa8c1b8b60cc567`  
		Last Modified: Thu, 14 Aug 2025 17:56:31 GMT  
		Size: 14.8 KB (14821 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.8-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e2578c673d8e347750aad6968df9283d0902cf83b36f7f52eaa2c169fde4886c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10409365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21abd46018664ec1d774ed0ccf028420f6687e33f812018fc3a910dc1ce6014`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdc9114678c7494cfff4d6d27e8c14856724b7b46c06d21e6f5309bb10cfd3e`  
		Last Modified: Thu, 14 Aug 2025 18:48:38 GMT  
		Size: 6.3 MB (6277644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9345987e164f0a7a3c9724b12596354d6f5b27a55c274c5943cf749ce9826044`  
		Last Modified: Thu, 14 Aug 2025 18:48:37 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac90761c84b8f60ad18110b9e9ff4b720ab1d809ff03b57faf042e634d59447`  
		Last Modified: Thu, 14 Aug 2025 18:48:38 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.8-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5b917f85bbda7141f8205a4c9d33e28145986c0124ea61f249bd1dbddc4eb538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b21a2426a39cfaf66ebf67d14f2866bfd16bf48c2083eed033b2421bd386a90`

```dockerfile
```

-	Layers:
	-	`sha256:e7738d4b72278c061ab6dd0a6f25f99f4c87e2797157b8dac4f79cea46c6760a`  
		Last Modified: Thu, 14 Aug 2025 20:56:49 GMT  
		Size: 14.9 KB (14865 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.8-alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:30ad03d77dfb5de88442d0f29c490713d82448efd77693faf7b0935a99453b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9985901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23f66326a77590bc41eb0a5f9f97a5c40ca317276be7cdaf7f7322df7416182`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3e45745642d3a22ccb49be50acc20c0214bd2a5273c0975019b6597df4b5d2`  
		Last Modified: Thu, 14 Aug 2025 18:56:45 GMT  
		Size: 6.3 MB (6257816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a20674adfb2e91f75f547789596c957e2840dfa110ac58dcec2f5e6b686fcd`  
		Last Modified: Thu, 14 Aug 2025 18:56:43 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f76e967ee5d9ae2c5527cef9bb9c8edd4f553ba6495330dc86ee3565f14fc6`  
		Last Modified: Thu, 14 Aug 2025 18:56:43 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.8-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:050addcc71308640a4197a465ab8b25fd37500d546c2fbade4232636badd6976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44be2d0d1465d7c59fd92abeb1e0ea0dc33b19b0122cfa12d0204c30e4d4ae13`

```dockerfile
```

-	Layers:
	-	`sha256:66f52a56e2b84f4136709b50caf6b3e34917205c3aeba573456e28d55213cdaa`  
		Last Modified: Thu, 14 Aug 2025 20:56:52 GMT  
		Size: 14.8 KB (14781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.8-alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:2bf7f126291a09aa21ef2c65fc041fedfe9e9e29e16a8858bf193280e1318fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10271313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e03788a43a2cfeaefbb6d84b08849b6b847b39eeab7af6cfa746c5475cc49a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813401984db76a6756e0db9016fe48ee5c9d82865d147dd243a26b51b2aad684`  
		Last Modified: Thu, 14 Aug 2025 18:35:37 GMT  
		Size: 6.6 MB (6625370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968c785997911db8d7fa72cfc92186b2fc98d2dd5485d575df8bede6c19e3837`  
		Last Modified: Thu, 14 Aug 2025 18:35:38 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5213bbb60ea3349a52da162a1ed048b3650fabc2973bb84980b33601e46410af`  
		Last Modified: Thu, 14 Aug 2025 18:35:37 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.8-alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:068c939c8d89bfd8a734c0c4fcb03e2f6122fb7cb278e2af5857d850feb3c05c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f0a7a9a995483ed6030887daaf0da034c453fa869bd81b7cb6c7e352c4e8daa`

```dockerfile
```

-	Layers:
	-	`sha256:4f8fbf204f658abfd1d495febd491047b4ab613c794be7a1f20e98c98ef2c224`  
		Last Modified: Thu, 14 Aug 2025 20:56:55 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.8-linux`

```console
$ docker pull nats@sha256:cba2e1f30fcec448bebbbe0ccd3c25e70716cc63c178c69c64297094b0e6eb37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `nats:2.11.8-linux` - linux; amd64

```console
$ docker pull nats@sha256:5634002bb5af84b0379f0de363bf0027b76bd6cf1a1db66ad254ae945a163cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6340078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d63b90f51c086da0db2adbc1a2ad7102ecabb8fa67c2470fdc2217b40a4d922`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b663fe8cd396789f2474139e39527f819c3a482db5e25e230cacaadd75df18ce`  
		Last Modified: Thu, 14 Aug 2025 17:27:46 GMT  
		Size: 6.3 MB (6339570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e38b65a6463af6a5ebdc0b02115f51a91399b2710a2758586bbeda7b6d50ba`  
		Last Modified: Thu, 14 Aug 2025 17:27:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.8-linux` - unknown; unknown

```console
$ docker pull nats@sha256:2ab05007143b6795815ff8714f15842e070df35013849973ca0b2f3552177ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310bb9bbe1f9febd06c494bb2dd5b961d7bf71acc8bf0b2fb53e0834a8cc2117`

```dockerfile
```

-	Layers:
	-	`sha256:85acdef1c273fe4667fee682e56c38f81137085631f156c2949814b3bc0d0bee`  
		Last Modified: Thu, 14 Aug 2025 20:56:26 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.8-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:40d95d59739fe46433103f4d262d1dd789f75ee44e99c640ea6457cf05487501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6054066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492743618ce250d8b5f53bf5f1e12404d57c3ec44625d5b44726e86f9bba5086`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f10f27efc9fb4dc2b4cdaada3f99aa2ffb9ebc99496fd55f1920263e51b914c9`  
		Last Modified: Thu, 14 Aug 2025 18:07:33 GMT  
		Size: 6.1 MB (6053556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bdfede140a8dbbb6956c184b88de98cc1662ecbef253a2a4433bc47021d07dc`  
		Last Modified: Thu, 14 Aug 2025 18:07:33 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.8-linux` - unknown; unknown

```console
$ docker pull nats@sha256:06dde395a53d1e08b8fd585a2037a3d0579d0cf26446b77df720fb5c757064f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b6f621ca40cc0a37945b871d68296b32cdb51732868485359bc907292b6eba`

```dockerfile
```

-	Layers:
	-	`sha256:6cffdd7549f5659166afe24fb85e23cfebf2409e108e1f347151569e8e28ba38`  
		Last Modified: Thu, 14 Aug 2025 20:56:30 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.8-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:815e928020aef447482878a6cef15fd72ac0f9d767b8309b032f7fb8feb7a353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6043424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbbf5945fb4360c4f621c54027b1cb47034cc2fa4d455ccc3f90923c1fe13761`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ba52e77e96ac90555714325e16a7b63d377c42dbeec68ba24cd503063cf7b9e0`  
		Last Modified: Thu, 14 Aug 2025 17:27:10 GMT  
		Size: 6.0 MB (6042914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ee5e05524b58d5802a62546f6f2347446d5321c4e8d583722db5b777d831d1`  
		Last Modified: Thu, 14 Aug 2025 17:27:08 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.8-linux` - unknown; unknown

```console
$ docker pull nats@sha256:842f4f4569460f34fc562978f687fc36581c388b02ab14cdad623893d588f5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2b1c717567f7faa2dde66fcb89acd6dcf382ec81408e1c26ecb2d68f03d105`

```dockerfile
```

-	Layers:
	-	`sha256:62da1307e4b0132c952bdd53d1b82eb3e96fa2934b1b582a8b7277351ddc31cd`  
		Last Modified: Thu, 14 Aug 2025 20:56:33 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.8-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d46af1d33927787659e676ea4714a6d53c8ba71956e0cda595d30ab277af5341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b7bb1d1d30e4a8233087664e0b5540f3e42f49f27589cfb43d23bacbeb63ffe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5823b59d47a0c660012e09655022b6660ce21c617ee2978f3edacb2ac344cb9f`  
		Last Modified: Thu, 14 Aug 2025 19:46:02 GMT  
		Size: 5.8 MB (5827281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e915dc222e2df5e58849a12f73e5fcede2bc08f2c98fd12f234ad34883849b`  
		Last Modified: Thu, 14 Aug 2025 19:46:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.8-linux` - unknown; unknown

```console
$ docker pull nats@sha256:4e9ff58758ddaea565568a15d4d049d69f51f01f69e9e0e517c68718dfe93ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a92dc3160475131a9aa4330ac0e14dedb97f5d4d57d5a386b4b1033afe203bc`

```dockerfile
```

-	Layers:
	-	`sha256:efd6b414c46e44a7c6cd8407e5887b4066f7e91785d16647bdfc24cb7dfb35a4`  
		Last Modified: Thu, 14 Aug 2025 20:56:36 GMT  
		Size: 10.6 KB (10649 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.8-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:70ad109d17470e9dbefe10df2ea372ea487e5a28cf96934110c5f6e6b118c4ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5807845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcf49d098aee252cf17a17945623b98c12312f01460230bd2494a20949c2703`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:221614c6b4427295323da315f973992219d61abd51aa73f549b80d617ceed783`  
		Last Modified: Thu, 14 Aug 2025 20:45:44 GMT  
		Size: 5.8 MB (5807337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea070ca5e9aa9e1edaa1764d931a0b0e385793e5b3124004b4ba91da5efc9e9`  
		Last Modified: Thu, 14 Aug 2025 20:45:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.8-linux` - unknown; unknown

```console
$ docker pull nats@sha256:bf4cec841a590e736bc48410cd41b4eb5176b07e39b161d5827a0dfe411fb72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd14ce8eff83929fceb915b93bd248d9837b402d7c289ab095bb35b5306608d`

```dockerfile
```

-	Layers:
	-	`sha256:f968b5bb7ad9cd95b31e5948c6d247e8ff2820fa830ca084746ac40f662b15d1`  
		Last Modified: Thu, 14 Aug 2025 23:56:26 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.8-nanoserver`

```console
$ docker pull nats@sha256:4b5bc1dda10956fffbd5637c74ca36f1f8e8999841816091381b80f7f4368b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2.11.8-nanoserver` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:ad9de8f09f3634777b25adb56728db4ae6804eb3e93cf167d338af2569150272
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129178975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3e567374bac2065f94b8560a0f1747b427e881b5faa654919d1f7abccc554d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Thu, 14 Aug 2025 18:14:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 14 Aug 2025 18:14:05 GMT
RUN cmd /S /C #(nop) COPY file:3fa3039439cf4074860757aeaaa6c458fcb2a8fd53320637e2edb93570462bde in C:\nats-server.exe 
# Thu, 14 Aug 2025 18:14:06 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Aug 2025 18:14:07 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 14 Aug 2025 18:14:08 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Aug 2025 18:14:09 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70dd762bbc2519848d92e4250ffd2e8ad506e67e2ccc6edb8b28deb7bd6a4cc3`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8303cc1b67f588378cd15d48f0f9092ea5f9e1d8e2832d99a509bdd9c8ff70a`  
		Last Modified: Thu, 14 Aug 2025 18:14:54 GMT  
		Size: 6.5 MB (6512850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5204fc3573607851e777581d8f3393c06877a1b385138e9ddb562e41c44ae04f`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5811e67cadd8e8c18aa9f537c4147610482318cb56ca5e6a1ff3cff5d96e4cfc`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b880e68edcdaf39200bd33cc61fd60fab56c1eae85a872652a20730da3d12a`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbef80910535149a3762e6bfc014c51084a8c11fa366889b246185411c39fb9`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.8-nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:4b5bc1dda10956fffbd5637c74ca36f1f8e8999841816091381b80f7f4368b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2.11.8-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:ad9de8f09f3634777b25adb56728db4ae6804eb3e93cf167d338af2569150272
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129178975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3e567374bac2065f94b8560a0f1747b427e881b5faa654919d1f7abccc554d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Thu, 14 Aug 2025 18:14:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 14 Aug 2025 18:14:05 GMT
RUN cmd /S /C #(nop) COPY file:3fa3039439cf4074860757aeaaa6c458fcb2a8fd53320637e2edb93570462bde in C:\nats-server.exe 
# Thu, 14 Aug 2025 18:14:06 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Aug 2025 18:14:07 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 14 Aug 2025 18:14:08 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Aug 2025 18:14:09 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70dd762bbc2519848d92e4250ffd2e8ad506e67e2ccc6edb8b28deb7bd6a4cc3`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8303cc1b67f588378cd15d48f0f9092ea5f9e1d8e2832d99a509bdd9c8ff70a`  
		Last Modified: Thu, 14 Aug 2025 18:14:54 GMT  
		Size: 6.5 MB (6512850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5204fc3573607851e777581d8f3393c06877a1b385138e9ddb562e41c44ae04f`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5811e67cadd8e8c18aa9f537c4147610482318cb56ca5e6a1ff3cff5d96e4cfc`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b880e68edcdaf39200bd33cc61fd60fab56c1eae85a872652a20730da3d12a`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbef80910535149a3762e6bfc014c51084a8c11fa366889b246185411c39fb9`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.8-scratch`

```console
$ docker pull nats@sha256:cba2e1f30fcec448bebbbe0ccd3c25e70716cc63c178c69c64297094b0e6eb37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `nats:2.11.8-scratch` - linux; amd64

```console
$ docker pull nats@sha256:5634002bb5af84b0379f0de363bf0027b76bd6cf1a1db66ad254ae945a163cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6340078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d63b90f51c086da0db2adbc1a2ad7102ecabb8fa67c2470fdc2217b40a4d922`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b663fe8cd396789f2474139e39527f819c3a482db5e25e230cacaadd75df18ce`  
		Last Modified: Thu, 14 Aug 2025 17:27:46 GMT  
		Size: 6.3 MB (6339570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e38b65a6463af6a5ebdc0b02115f51a91399b2710a2758586bbeda7b6d50ba`  
		Last Modified: Thu, 14 Aug 2025 17:27:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.8-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:2ab05007143b6795815ff8714f15842e070df35013849973ca0b2f3552177ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310bb9bbe1f9febd06c494bb2dd5b961d7bf71acc8bf0b2fb53e0834a8cc2117`

```dockerfile
```

-	Layers:
	-	`sha256:85acdef1c273fe4667fee682e56c38f81137085631f156c2949814b3bc0d0bee`  
		Last Modified: Thu, 14 Aug 2025 20:56:26 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.8-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:40d95d59739fe46433103f4d262d1dd789f75ee44e99c640ea6457cf05487501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6054066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492743618ce250d8b5f53bf5f1e12404d57c3ec44625d5b44726e86f9bba5086`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f10f27efc9fb4dc2b4cdaada3f99aa2ffb9ebc99496fd55f1920263e51b914c9`  
		Last Modified: Thu, 14 Aug 2025 18:07:33 GMT  
		Size: 6.1 MB (6053556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bdfede140a8dbbb6956c184b88de98cc1662ecbef253a2a4433bc47021d07dc`  
		Last Modified: Thu, 14 Aug 2025 18:07:33 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.8-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:06dde395a53d1e08b8fd585a2037a3d0579d0cf26446b77df720fb5c757064f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b6f621ca40cc0a37945b871d68296b32cdb51732868485359bc907292b6eba`

```dockerfile
```

-	Layers:
	-	`sha256:6cffdd7549f5659166afe24fb85e23cfebf2409e108e1f347151569e8e28ba38`  
		Last Modified: Thu, 14 Aug 2025 20:56:30 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.8-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:815e928020aef447482878a6cef15fd72ac0f9d767b8309b032f7fb8feb7a353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6043424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbbf5945fb4360c4f621c54027b1cb47034cc2fa4d455ccc3f90923c1fe13761`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ba52e77e96ac90555714325e16a7b63d377c42dbeec68ba24cd503063cf7b9e0`  
		Last Modified: Thu, 14 Aug 2025 17:27:10 GMT  
		Size: 6.0 MB (6042914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ee5e05524b58d5802a62546f6f2347446d5321c4e8d583722db5b777d831d1`  
		Last Modified: Thu, 14 Aug 2025 17:27:08 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.8-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:842f4f4569460f34fc562978f687fc36581c388b02ab14cdad623893d588f5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2b1c717567f7faa2dde66fcb89acd6dcf382ec81408e1c26ecb2d68f03d105`

```dockerfile
```

-	Layers:
	-	`sha256:62da1307e4b0132c952bdd53d1b82eb3e96fa2934b1b582a8b7277351ddc31cd`  
		Last Modified: Thu, 14 Aug 2025 20:56:33 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.8-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d46af1d33927787659e676ea4714a6d53c8ba71956e0cda595d30ab277af5341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b7bb1d1d30e4a8233087664e0b5540f3e42f49f27589cfb43d23bacbeb63ffe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5823b59d47a0c660012e09655022b6660ce21c617ee2978f3edacb2ac344cb9f`  
		Last Modified: Thu, 14 Aug 2025 19:46:02 GMT  
		Size: 5.8 MB (5827281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e915dc222e2df5e58849a12f73e5fcede2bc08f2c98fd12f234ad34883849b`  
		Last Modified: Thu, 14 Aug 2025 19:46:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.8-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4e9ff58758ddaea565568a15d4d049d69f51f01f69e9e0e517c68718dfe93ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a92dc3160475131a9aa4330ac0e14dedb97f5d4d57d5a386b4b1033afe203bc`

```dockerfile
```

-	Layers:
	-	`sha256:efd6b414c46e44a7c6cd8407e5887b4066f7e91785d16647bdfc24cb7dfb35a4`  
		Last Modified: Thu, 14 Aug 2025 20:56:36 GMT  
		Size: 10.6 KB (10649 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2.11.8-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:70ad109d17470e9dbefe10df2ea372ea487e5a28cf96934110c5f6e6b118c4ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5807845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcf49d098aee252cf17a17945623b98c12312f01460230bd2494a20949c2703`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:221614c6b4427295323da315f973992219d61abd51aa73f549b80d617ceed783`  
		Last Modified: Thu, 14 Aug 2025 20:45:44 GMT  
		Size: 5.8 MB (5807337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea070ca5e9aa9e1edaa1764d931a0b0e385793e5b3124004b4ba91da5efc9e9`  
		Last Modified: Thu, 14 Aug 2025 20:45:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2.11.8-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:bf4cec841a590e736bc48410cd41b4eb5176b07e39b161d5827a0dfe411fb72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd14ce8eff83929fceb915b93bd248d9837b402d7c289ab095bb35b5306608d`

```dockerfile
```

-	Layers:
	-	`sha256:f968b5bb7ad9cd95b31e5948c6d247e8ff2820fa830ca084746ac40f662b15d1`  
		Last Modified: Thu, 14 Aug 2025 23:56:26 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:2.11.8-windowsservercore`

```console
$ docker pull nats@sha256:cd40ad4037d8bcb19778d0ec3407978059ea88d895747dfce3ea1be3f83f5760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2.11.8-windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:ff0d0047ceb610a0b73edcb6d12305bdf06e08a127258cf923e1aec9645ec419
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2288892735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe5b93e3cd45a63955014ff0d53cf5383f91b868d6bacf1c242ce4861d0a3fe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Thu, 14 Aug 2025 17:24:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 14 Aug 2025 17:24:18 GMT
ENV NATS_DOCKERIZED=1
# Thu, 14 Aug 2025 17:24:19 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 17:24:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.8/nats-server-v2.11.8-windows-amd64.zip
# Thu, 14 Aug 2025 17:24:21 GMT
ENV NATS_SERVER_SHASUM=3dd98465626e8c6ed92a784ef13c3f956c7e87fbbb4ee86cc198e377565eaeaf
# Thu, 14 Aug 2025 17:24:28 GMT
RUN Set-PSDebug -Trace 2
# Thu, 14 Aug 2025 17:24:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 14 Aug 2025 17:24:44 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Aug 2025 17:24:45 GMT
EXPOSE 4222 6222 8222
# Thu, 14 Aug 2025 17:24:46 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Aug 2025 17:24:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3f006d1cb294833347c0dcdeff82dda52af9acbea696337fd8408869317713`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e0fe1f9e451f5b78de6f2eabbcf9dd583e44cc8efca284c024e6fc31fea206`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4c9efb293cf4538944d58d49d978df5a06ed2586f43c0312291c6ed0854b98`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4fcdec518a7d5e9cbdbb2398711d526df04c6abd46f6dc74c91ce20cb62a28`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f32d8dbe729b86cde1eafd2da61359f32dab9aa4ff767aa70b3dc9351ba01c3`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1453289e44dd8e7a29b2a8395640bb6a2e2ebd47060a6bfe129031ce2072d7`  
		Last Modified: Thu, 14 Aug 2025 17:26:08 GMT  
		Size: 336.2 KB (336246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db38558f3d85860c055f99e79e865d42a17dd691a4f83ea93e0f8a5e391d125`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 6.9 MB (6852407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb87097b18d82c7dc42b80c5f6912e34cd08ecb316ffd445266fbb02ee18352b`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828b5772011538e3bb3bd9055b2b9e9b10bb6ffd46dc54a1d765d3e2dcfb03a6`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd3abb758a5b3c339001a04d7364df2b54b00e27711aecf5f44a76323ef676f`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366367ce039c79734b9ad15e13867ea0fd5f18ee46cc185dde59b3507a9b3392`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.11.8-windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:cd40ad4037d8bcb19778d0ec3407978059ea88d895747dfce3ea1be3f83f5760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:2.11.8-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:ff0d0047ceb610a0b73edcb6d12305bdf06e08a127258cf923e1aec9645ec419
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2288892735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe5b93e3cd45a63955014ff0d53cf5383f91b868d6bacf1c242ce4861d0a3fe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Thu, 14 Aug 2025 17:24:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 14 Aug 2025 17:24:18 GMT
ENV NATS_DOCKERIZED=1
# Thu, 14 Aug 2025 17:24:19 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 17:24:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.8/nats-server-v2.11.8-windows-amd64.zip
# Thu, 14 Aug 2025 17:24:21 GMT
ENV NATS_SERVER_SHASUM=3dd98465626e8c6ed92a784ef13c3f956c7e87fbbb4ee86cc198e377565eaeaf
# Thu, 14 Aug 2025 17:24:28 GMT
RUN Set-PSDebug -Trace 2
# Thu, 14 Aug 2025 17:24:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 14 Aug 2025 17:24:44 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Aug 2025 17:24:45 GMT
EXPOSE 4222 6222 8222
# Thu, 14 Aug 2025 17:24:46 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Aug 2025 17:24:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3f006d1cb294833347c0dcdeff82dda52af9acbea696337fd8408869317713`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e0fe1f9e451f5b78de6f2eabbcf9dd583e44cc8efca284c024e6fc31fea206`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4c9efb293cf4538944d58d49d978df5a06ed2586f43c0312291c6ed0854b98`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4fcdec518a7d5e9cbdbb2398711d526df04c6abd46f6dc74c91ce20cb62a28`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f32d8dbe729b86cde1eafd2da61359f32dab9aa4ff767aa70b3dc9351ba01c3`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1453289e44dd8e7a29b2a8395640bb6a2e2ebd47060a6bfe129031ce2072d7`  
		Last Modified: Thu, 14 Aug 2025 17:26:08 GMT  
		Size: 336.2 KB (336246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db38558f3d85860c055f99e79e865d42a17dd691a4f83ea93e0f8a5e391d125`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 6.9 MB (6852407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb87097b18d82c7dc42b80c5f6912e34cd08ecb316ffd445266fbb02ee18352b`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828b5772011538e3bb3bd9055b2b9e9b10bb6ffd46dc54a1d765d3e2dcfb03a6`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd3abb758a5b3c339001a04d7364df2b54b00e27711aecf5f44a76323ef676f`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366367ce039c79734b9ad15e13867ea0fd5f18ee46cc185dde59b3507a9b3392`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine`

```console
$ docker pull nats@sha256:71092f77d707a4a81b12aca5096d6b2d2e07ad16aa57c84066940a17af74f61a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:9e5633ac7584fc4e80d34be3ff7e15aa3fabec79a5573c2d9abefcf1f7761d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10586751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dfa54630538e8565a0953e5d7316c4b92bd17e293ec333e94f52be2094e7300`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ab6e8880f219a2dd7752796195d9939c137da1ea12c10015c60812ca497573`  
		Last Modified: Thu, 14 Aug 2025 17:21:49 GMT  
		Size: 6.8 MB (6786090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283833608b5ae7ddb376c701f296ad922908c7627de5632ba6e83601e7ac8355`  
		Last Modified: Thu, 14 Aug 2025 17:21:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3411c495c894b3b46ad114eceb39fb6deff204dacab199804c51fd2e1a33a5ae`  
		Last Modified: Thu, 14 Aug 2025 17:21:49 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:d90e427f49684d9b241e599c42a542365675aa62dd6d92a617694d503903cfcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299652c57abf36d15568386e529c8a81ada9d5600ced03a88bccc20b7a50be31`

```dockerfile
```

-	Layers:
	-	`sha256:4ff271d6ce9dacd8101fce3d16eda36e2bbe12422efe9c37df07a8f681004669`  
		Last Modified: Thu, 14 Aug 2025 17:56:25 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:2cfaa354cfe1d863108af5b170d266f632b75f3785be68158e9e0cd1170c640a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10004611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:decbc388e2e168ea436dfa71f5e8cac800997860eb2b021cab4f5e4eec76027f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381ebd5419e3fec8229c2bc4e50847a161b2d4865cfcb4e6733a0ea3c32c77b4`  
		Last Modified: Thu, 14 Aug 2025 18:30:15 GMT  
		Size: 6.5 MB (6502730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37fce2ec2d65289a1c9ac7f39b6ae87b35135e3b107484e7e844793f8d7ff565`  
		Last Modified: Thu, 14 Aug 2025 17:37:15 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872252a349b6a653af65ab2ffc9f0d3cf5eeca6d0e42153f5c303d068d5e1812`  
		Last Modified: Thu, 14 Aug 2025 17:37:18 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:14ef749c437d808301a1efe45e399507ff98890b94c616d0007f1534cc8ab482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac20fd9b620208d75d0fd87edc4b9f19c291e788b7e21cc16cbdb65e53dac741`

```dockerfile
```

-	Layers:
	-	`sha256:57504cb714044ba92951c29c12ec66ede4547725749d0a068268c4cb751a035d`  
		Last Modified: Thu, 14 Aug 2025 20:56:44 GMT  
		Size: 14.8 KB (14821 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:1dc6b44e4b33dbe327dda601fff6bb363ef44c34a4ab2177f307f2d9937f49a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9712521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8885fe376c67ec4357739c5950356acebf63efd04e908fdd24e82f77fbfc7511`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b47ccb42d9de5fae140120c5d63f9ac56f0c1a50c858bfdb2926a8b8c9fa01`  
		Last Modified: Thu, 14 Aug 2025 17:20:49 GMT  
		Size: 6.5 MB (6492514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ae165d2cd161f3b90c15a6ebf63ef30cd24b1314b6c1c9ccfdfe1929e38949`  
		Last Modified: Thu, 14 Aug 2025 17:20:49 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0ad244a682bc355346daaf39628ff905c5a9830e058a1e989c513f9abf0f34`  
		Last Modified: Thu, 14 Aug 2025 17:20:49 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:f63e9df6411bb2032dedb0fe108e98c278fa2dc1239ac4181f3aefe3dc522497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e855d196a62bbe9f94bd2c44e04b0d5cacb3afdcd63e28f775fa65001122f6a0`

```dockerfile
```

-	Layers:
	-	`sha256:d69e84adacba24383fb74725a58e3be312fd8246fa5942fd3aa8c1b8b60cc567`  
		Last Modified: Thu, 14 Aug 2025 17:56:31 GMT  
		Size: 14.8 KB (14821 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e2578c673d8e347750aad6968df9283d0902cf83b36f7f52eaa2c169fde4886c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10409365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21abd46018664ec1d774ed0ccf028420f6687e33f812018fc3a910dc1ce6014`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdc9114678c7494cfff4d6d27e8c14856724b7b46c06d21e6f5309bb10cfd3e`  
		Last Modified: Thu, 14 Aug 2025 18:48:38 GMT  
		Size: 6.3 MB (6277644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9345987e164f0a7a3c9724b12596354d6f5b27a55c274c5943cf749ce9826044`  
		Last Modified: Thu, 14 Aug 2025 18:48:37 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac90761c84b8f60ad18110b9e9ff4b720ab1d809ff03b57faf042e634d59447`  
		Last Modified: Thu, 14 Aug 2025 18:48:38 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5b917f85bbda7141f8205a4c9d33e28145986c0124ea61f249bd1dbddc4eb538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b21a2426a39cfaf66ebf67d14f2866bfd16bf48c2083eed033b2421bd386a90`

```dockerfile
```

-	Layers:
	-	`sha256:e7738d4b72278c061ab6dd0a6f25f99f4c87e2797157b8dac4f79cea46c6760a`  
		Last Modified: Thu, 14 Aug 2025 20:56:49 GMT  
		Size: 14.9 KB (14865 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:30ad03d77dfb5de88442d0f29c490713d82448efd77693faf7b0935a99453b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9985901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23f66326a77590bc41eb0a5f9f97a5c40ca317276be7cdaf7f7322df7416182`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3e45745642d3a22ccb49be50acc20c0214bd2a5273c0975019b6597df4b5d2`  
		Last Modified: Thu, 14 Aug 2025 18:56:45 GMT  
		Size: 6.3 MB (6257816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a20674adfb2e91f75f547789596c957e2840dfa110ac58dcec2f5e6b686fcd`  
		Last Modified: Thu, 14 Aug 2025 18:56:43 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f76e967ee5d9ae2c5527cef9bb9c8edd4f553ba6495330dc86ee3565f14fc6`  
		Last Modified: Thu, 14 Aug 2025 18:56:43 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:050addcc71308640a4197a465ab8b25fd37500d546c2fbade4232636badd6976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44be2d0d1465d7c59fd92abeb1e0ea0dc33b19b0122cfa12d0204c30e4d4ae13`

```dockerfile
```

-	Layers:
	-	`sha256:66f52a56e2b84f4136709b50caf6b3e34917205c3aeba573456e28d55213cdaa`  
		Last Modified: Thu, 14 Aug 2025 20:56:52 GMT  
		Size: 14.8 KB (14781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine` - linux; s390x

```console
$ docker pull nats@sha256:2bf7f126291a09aa21ef2c65fc041fedfe9e9e29e16a8858bf193280e1318fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10271313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e03788a43a2cfeaefbb6d84b08849b6b847b39eeab7af6cfa746c5475cc49a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813401984db76a6756e0db9016fe48ee5c9d82865d147dd243a26b51b2aad684`  
		Last Modified: Thu, 14 Aug 2025 18:35:37 GMT  
		Size: 6.6 MB (6625370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968c785997911db8d7fa72cfc92186b2fc98d2dd5485d575df8bede6c19e3837`  
		Last Modified: Thu, 14 Aug 2025 18:35:38 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5213bbb60ea3349a52da162a1ed048b3650fabc2973bb84980b33601e46410af`  
		Last Modified: Thu, 14 Aug 2025 18:35:37 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine` - unknown; unknown

```console
$ docker pull nats@sha256:068c939c8d89bfd8a734c0c4fcb03e2f6122fb7cb278e2af5857d850feb3c05c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f0a7a9a995483ed6030887daaf0da034c453fa869bd81b7cb6c7e352c4e8daa`

```dockerfile
```

-	Layers:
	-	`sha256:4f8fbf204f658abfd1d495febd491047b4ab613c794be7a1f20e98c98ef2c224`  
		Last Modified: Thu, 14 Aug 2025 20:56:55 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:alpine3.22`

```console
$ docker pull nats@sha256:71092f77d707a4a81b12aca5096d6b2d2e07ad16aa57c84066940a17af74f61a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:9e5633ac7584fc4e80d34be3ff7e15aa3fabec79a5573c2d9abefcf1f7761d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10586751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dfa54630538e8565a0953e5d7316c4b92bd17e293ec333e94f52be2094e7300`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ab6e8880f219a2dd7752796195d9939c137da1ea12c10015c60812ca497573`  
		Last Modified: Thu, 14 Aug 2025 17:21:49 GMT  
		Size: 6.8 MB (6786090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283833608b5ae7ddb376c701f296ad922908c7627de5632ba6e83601e7ac8355`  
		Last Modified: Thu, 14 Aug 2025 17:21:49 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3411c495c894b3b46ad114eceb39fb6deff204dacab199804c51fd2e1a33a5ae`  
		Last Modified: Thu, 14 Aug 2025 17:21:49 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:d90e427f49684d9b241e599c42a542365675aa62dd6d92a617694d503903cfcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299652c57abf36d15568386e529c8a81ada9d5600ced03a88bccc20b7a50be31`

```dockerfile
```

-	Layers:
	-	`sha256:4ff271d6ce9dacd8101fce3d16eda36e2bbe12422efe9c37df07a8f681004669`  
		Last Modified: Thu, 14 Aug 2025 17:56:25 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:2cfaa354cfe1d863108af5b170d266f632b75f3785be68158e9e0cd1170c640a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10004611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:decbc388e2e168ea436dfa71f5e8cac800997860eb2b021cab4f5e4eec76027f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381ebd5419e3fec8229c2bc4e50847a161b2d4865cfcb4e6733a0ea3c32c77b4`  
		Last Modified: Thu, 14 Aug 2025 18:30:15 GMT  
		Size: 6.5 MB (6502730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37fce2ec2d65289a1c9ac7f39b6ae87b35135e3b107484e7e844793f8d7ff565`  
		Last Modified: Thu, 14 Aug 2025 17:37:15 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872252a349b6a653af65ab2ffc9f0d3cf5eeca6d0e42153f5c303d068d5e1812`  
		Last Modified: Thu, 14 Aug 2025 17:37:18 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:14ef749c437d808301a1efe45e399507ff98890b94c616d0007f1534cc8ab482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac20fd9b620208d75d0fd87edc4b9f19c291e788b7e21cc16cbdb65e53dac741`

```dockerfile
```

-	Layers:
	-	`sha256:57504cb714044ba92951c29c12ec66ede4547725749d0a068268c4cb751a035d`  
		Last Modified: Thu, 14 Aug 2025 20:56:44 GMT  
		Size: 14.8 KB (14821 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:1dc6b44e4b33dbe327dda601fff6bb363ef44c34a4ab2177f307f2d9937f49a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9712521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8885fe376c67ec4357739c5950356acebf63efd04e908fdd24e82f77fbfc7511`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b47ccb42d9de5fae140120c5d63f9ac56f0c1a50c858bfdb2926a8b8c9fa01`  
		Last Modified: Thu, 14 Aug 2025 17:20:49 GMT  
		Size: 6.5 MB (6492514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ae165d2cd161f3b90c15a6ebf63ef30cd24b1314b6c1c9ccfdfe1929e38949`  
		Last Modified: Thu, 14 Aug 2025 17:20:49 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0ad244a682bc355346daaf39628ff905c5a9830e058a1e989c513f9abf0f34`  
		Last Modified: Thu, 14 Aug 2025 17:20:49 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:f63e9df6411bb2032dedb0fe108e98c278fa2dc1239ac4181f3aefe3dc522497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e855d196a62bbe9f94bd2c44e04b0d5cacb3afdcd63e28f775fa65001122f6a0`

```dockerfile
```

-	Layers:
	-	`sha256:d69e84adacba24383fb74725a58e3be312fd8246fa5942fd3aa8c1b8b60cc567`  
		Last Modified: Thu, 14 Aug 2025 17:56:31 GMT  
		Size: 14.8 KB (14821 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e2578c673d8e347750aad6968df9283d0902cf83b36f7f52eaa2c169fde4886c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10409365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21abd46018664ec1d774ed0ccf028420f6687e33f812018fc3a910dc1ce6014`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdc9114678c7494cfff4d6d27e8c14856724b7b46c06d21e6f5309bb10cfd3e`  
		Last Modified: Thu, 14 Aug 2025 18:48:38 GMT  
		Size: 6.3 MB (6277644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9345987e164f0a7a3c9724b12596354d6f5b27a55c274c5943cf749ce9826044`  
		Last Modified: Thu, 14 Aug 2025 18:48:37 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac90761c84b8f60ad18110b9e9ff4b720ab1d809ff03b57faf042e634d59447`  
		Last Modified: Thu, 14 Aug 2025 18:48:38 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:5b917f85bbda7141f8205a4c9d33e28145986c0124ea61f249bd1dbddc4eb538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b21a2426a39cfaf66ebf67d14f2866bfd16bf48c2083eed033b2421bd386a90`

```dockerfile
```

-	Layers:
	-	`sha256:e7738d4b72278c061ab6dd0a6f25f99f4c87e2797157b8dac4f79cea46c6760a`  
		Last Modified: Thu, 14 Aug 2025 20:56:49 GMT  
		Size: 14.9 KB (14865 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:30ad03d77dfb5de88442d0f29c490713d82448efd77693faf7b0935a99453b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9985901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23f66326a77590bc41eb0a5f9f97a5c40ca317276be7cdaf7f7322df7416182`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3e45745642d3a22ccb49be50acc20c0214bd2a5273c0975019b6597df4b5d2`  
		Last Modified: Thu, 14 Aug 2025 18:56:45 GMT  
		Size: 6.3 MB (6257816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a20674adfb2e91f75f547789596c957e2840dfa110ac58dcec2f5e6b686fcd`  
		Last Modified: Thu, 14 Aug 2025 18:56:43 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f76e967ee5d9ae2c5527cef9bb9c8edd4f553ba6495330dc86ee3565f14fc6`  
		Last Modified: Thu, 14 Aug 2025 18:56:43 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:050addcc71308640a4197a465ab8b25fd37500d546c2fbade4232636badd6976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44be2d0d1465d7c59fd92abeb1e0ea0dc33b19b0122cfa12d0204c30e4d4ae13`

```dockerfile
```

-	Layers:
	-	`sha256:66f52a56e2b84f4136709b50caf6b3e34917205c3aeba573456e28d55213cdaa`  
		Last Modified: Thu, 14 Aug 2025 20:56:52 GMT  
		Size: 14.8 KB (14781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:2bf7f126291a09aa21ef2c65fc041fedfe9e9e29e16a8858bf193280e1318fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10271313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e03788a43a2cfeaefbb6d84b08849b6b847b39eeab7af6cfa746c5475cc49a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 15:30:07 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='b08936cb1dc0ae7086137bda14c352df64397c4af45ed2b392705c19585aeb84' ;;     armhf) natsArch='arm6'; sha256='77508bd9f79b01a2b431393e4ba72004f57a07457793faeb366358512d3a1b91' ;;     armv7) natsArch='arm7'; sha256='271c4de30cdb5449f37709c5e64ec02f436aa489d309c5a5f64b46fa32d2000b' ;;     x86_64) natsArch='amd64'; sha256='397a6deffb5533e160de0cca322bc3dcaec7fb7282d66a3dfa87a9c183152ad1' ;;     x86) natsArch='386'; sha256='b12893ba9aa5a546c23cfd0c87f0afa44482d51ed850b8e171d6e543c126336e' ;;     s390x) natsArch='s390x'; sha256='6bf3289351dfb8805033802fbc9fc75a8a1329eccbca6e4074f7b8c2dcc5f8fb' ;;     ppc64le) natsArch='ppc64le'; sha256='d6ca70a7779057ec386bc29fce8a8f2c280ace83a20398af4592c25379539ee2' ;;     loong64) natsArch='loong64'; sha256='d4e3dc74fbc14afea6ca474a93a01e7a7028fab14fb622d4ac12c760f88bfbc9' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813401984db76a6756e0db9016fe48ee5c9d82865d147dd243a26b51b2aad684`  
		Last Modified: Thu, 14 Aug 2025 18:35:37 GMT  
		Size: 6.6 MB (6625370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968c785997911db8d7fa72cfc92186b2fc98d2dd5485d575df8bede6c19e3837`  
		Last Modified: Thu, 14 Aug 2025 18:35:38 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5213bbb60ea3349a52da162a1ed048b3650fabc2973bb84980b33601e46410af`  
		Last Modified: Thu, 14 Aug 2025 18:35:37 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:068c939c8d89bfd8a734c0c4fcb03e2f6122fb7cb278e2af5857d850feb3c05c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f0a7a9a995483ed6030887daaf0da034c453fa869bd81b7cb6c7e352c4e8daa`

```dockerfile
```

-	Layers:
	-	`sha256:4f8fbf204f658abfd1d495febd491047b4ab613c794be7a1f20e98c98ef2c224`  
		Last Modified: Thu, 14 Aug 2025 20:56:55 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:latest`

```console
$ docker pull nats@sha256:86e9fe3e8d887ea2c12322b4231c1f2f64e3c5b9917168198e1ab6c0fe16b222
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.20348.4052; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:5634002bb5af84b0379f0de363bf0027b76bd6cf1a1db66ad254ae945a163cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6340078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d63b90f51c086da0db2adbc1a2ad7102ecabb8fa67c2470fdc2217b40a4d922`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b663fe8cd396789f2474139e39527f819c3a482db5e25e230cacaadd75df18ce`  
		Last Modified: Thu, 14 Aug 2025 17:27:46 GMT  
		Size: 6.3 MB (6339570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e38b65a6463af6a5ebdc0b02115f51a91399b2710a2758586bbeda7b6d50ba`  
		Last Modified: Thu, 14 Aug 2025 17:27:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:2ab05007143b6795815ff8714f15842e070df35013849973ca0b2f3552177ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310bb9bbe1f9febd06c494bb2dd5b961d7bf71acc8bf0b2fb53e0834a8cc2117`

```dockerfile
```

-	Layers:
	-	`sha256:85acdef1c273fe4667fee682e56c38f81137085631f156c2949814b3bc0d0bee`  
		Last Modified: Thu, 14 Aug 2025 20:56:26 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:40d95d59739fe46433103f4d262d1dd789f75ee44e99c640ea6457cf05487501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6054066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492743618ce250d8b5f53bf5f1e12404d57c3ec44625d5b44726e86f9bba5086`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f10f27efc9fb4dc2b4cdaada3f99aa2ffb9ebc99496fd55f1920263e51b914c9`  
		Last Modified: Thu, 14 Aug 2025 18:07:33 GMT  
		Size: 6.1 MB (6053556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bdfede140a8dbbb6956c184b88de98cc1662ecbef253a2a4433bc47021d07dc`  
		Last Modified: Thu, 14 Aug 2025 18:07:33 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:06dde395a53d1e08b8fd585a2037a3d0579d0cf26446b77df720fb5c757064f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b6f621ca40cc0a37945b871d68296b32cdb51732868485359bc907292b6eba`

```dockerfile
```

-	Layers:
	-	`sha256:6cffdd7549f5659166afe24fb85e23cfebf2409e108e1f347151569e8e28ba38`  
		Last Modified: Thu, 14 Aug 2025 20:56:30 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:815e928020aef447482878a6cef15fd72ac0f9d767b8309b032f7fb8feb7a353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6043424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbbf5945fb4360c4f621c54027b1cb47034cc2fa4d455ccc3f90923c1fe13761`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ba52e77e96ac90555714325e16a7b63d377c42dbeec68ba24cd503063cf7b9e0`  
		Last Modified: Thu, 14 Aug 2025 17:27:10 GMT  
		Size: 6.0 MB (6042914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ee5e05524b58d5802a62546f6f2347446d5321c4e8d583722db5b777d831d1`  
		Last Modified: Thu, 14 Aug 2025 17:27:08 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:842f4f4569460f34fc562978f687fc36581c388b02ab14cdad623893d588f5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2b1c717567f7faa2dde66fcb89acd6dcf382ec81408e1c26ecb2d68f03d105`

```dockerfile
```

-	Layers:
	-	`sha256:62da1307e4b0132c952bdd53d1b82eb3e96fa2934b1b582a8b7277351ddc31cd`  
		Last Modified: Thu, 14 Aug 2025 20:56:33 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d46af1d33927787659e676ea4714a6d53c8ba71956e0cda595d30ab277af5341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b7bb1d1d30e4a8233087664e0b5540f3e42f49f27589cfb43d23bacbeb63ffe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5823b59d47a0c660012e09655022b6660ce21c617ee2978f3edacb2ac344cb9f`  
		Last Modified: Thu, 14 Aug 2025 19:46:02 GMT  
		Size: 5.8 MB (5827281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e915dc222e2df5e58849a12f73e5fcede2bc08f2c98fd12f234ad34883849b`  
		Last Modified: Thu, 14 Aug 2025 19:46:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:4e9ff58758ddaea565568a15d4d049d69f51f01f69e9e0e517c68718dfe93ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a92dc3160475131a9aa4330ac0e14dedb97f5d4d57d5a386b4b1033afe203bc`

```dockerfile
```

-	Layers:
	-	`sha256:efd6b414c46e44a7c6cd8407e5887b4066f7e91785d16647bdfc24cb7dfb35a4`  
		Last Modified: Thu, 14 Aug 2025 20:56:36 GMT  
		Size: 10.6 KB (10649 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; ppc64le

```console
$ docker pull nats@sha256:70ad109d17470e9dbefe10df2ea372ea487e5a28cf96934110c5f6e6b118c4ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5807845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcf49d098aee252cf17a17945623b98c12312f01460230bd2494a20949c2703`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:221614c6b4427295323da315f973992219d61abd51aa73f549b80d617ceed783`  
		Last Modified: Thu, 14 Aug 2025 20:45:44 GMT  
		Size: 5.8 MB (5807337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea070ca5e9aa9e1edaa1764d931a0b0e385793e5b3124004b4ba91da5efc9e9`  
		Last Modified: Thu, 14 Aug 2025 20:45:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:bf4cec841a590e736bc48410cd41b4eb5176b07e39b161d5827a0dfe411fb72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd14ce8eff83929fceb915b93bd248d9837b402d7c289ab095bb35b5306608d`

```dockerfile
```

-	Layers:
	-	`sha256:f968b5bb7ad9cd95b31e5948c6d247e8ff2820fa830ca084746ac40f662b15d1`  
		Last Modified: Thu, 14 Aug 2025 23:56:26 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - linux; s390x

```console
$ docker pull nats@sha256:66e24c97e22fd4db570efbde5c154dad761a934509688d1066ff6faf16c6ff8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6173621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5239fb0f4852c75ada10240d6ad54ccabbe1c300c54385271ab0d9c9a16d599`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 Aug 2025 12:51:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 Aug 2025 12:51:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 Aug 2025 12:51:02 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 Aug 2025 12:51:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 Aug 2025 12:51:02 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 Aug 2025 12:51:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:84a200250dfb971cfcf23197670e7ccfcfae55787bc8842c737081462376b978`  
		Last Modified: Mon, 04 Aug 2025 18:10:15 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5013d749e0797d9a012b7f969383e42b359cae57b7b1945f62eae07e6f12bbb`  
		Last Modified: Mon, 04 Aug 2025 18:10:15 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:latest` - unknown; unknown

```console
$ docker pull nats@sha256:3e90c2e5acc844d0189d6d664df76b3fc55d6438e1be7c1146763d00098ed8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469d8c0a969e19358745ad9513225279dd13b3d004003729b94ccd524773ffb5`

```dockerfile
```

-	Layers:
	-	`sha256:3490df75b7ac2f5425cf2a5decc578d60f595e9e0317faa4e73c20548b16f138`  
		Last Modified: Mon, 04 Aug 2025 20:56:51 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:latest` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:ad9de8f09f3634777b25adb56728db4ae6804eb3e93cf167d338af2569150272
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129178975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3e567374bac2065f94b8560a0f1747b427e881b5faa654919d1f7abccc554d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Thu, 14 Aug 2025 18:14:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 14 Aug 2025 18:14:05 GMT
RUN cmd /S /C #(nop) COPY file:3fa3039439cf4074860757aeaaa6c458fcb2a8fd53320637e2edb93570462bde in C:\nats-server.exe 
# Thu, 14 Aug 2025 18:14:06 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Aug 2025 18:14:07 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 14 Aug 2025 18:14:08 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Aug 2025 18:14:09 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70dd762bbc2519848d92e4250ffd2e8ad506e67e2ccc6edb8b28deb7bd6a4cc3`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8303cc1b67f588378cd15d48f0f9092ea5f9e1d8e2832d99a509bdd9c8ff70a`  
		Last Modified: Thu, 14 Aug 2025 18:14:54 GMT  
		Size: 6.5 MB (6512850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5204fc3573607851e777581d8f3393c06877a1b385138e9ddb562e41c44ae04f`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5811e67cadd8e8c18aa9f537c4147610482318cb56ca5e6a1ff3cff5d96e4cfc`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b880e68edcdaf39200bd33cc61fd60fab56c1eae85a872652a20730da3d12a`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbef80910535149a3762e6bfc014c51084a8c11fa366889b246185411c39fb9`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:afa7b504a629a7e9f8b4a3984a4dd796fe58a5267adbe0c18af723277657af7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:5634002bb5af84b0379f0de363bf0027b76bd6cf1a1db66ad254ae945a163cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6340078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d63b90f51c086da0db2adbc1a2ad7102ecabb8fa67c2470fdc2217b40a4d922`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b663fe8cd396789f2474139e39527f819c3a482db5e25e230cacaadd75df18ce`  
		Last Modified: Thu, 14 Aug 2025 17:27:46 GMT  
		Size: 6.3 MB (6339570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e38b65a6463af6a5ebdc0b02115f51a91399b2710a2758586bbeda7b6d50ba`  
		Last Modified: Thu, 14 Aug 2025 17:27:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:2ab05007143b6795815ff8714f15842e070df35013849973ca0b2f3552177ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310bb9bbe1f9febd06c494bb2dd5b961d7bf71acc8bf0b2fb53e0834a8cc2117`

```dockerfile
```

-	Layers:
	-	`sha256:85acdef1c273fe4667fee682e56c38f81137085631f156c2949814b3bc0d0bee`  
		Last Modified: Thu, 14 Aug 2025 20:56:26 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:40d95d59739fe46433103f4d262d1dd789f75ee44e99c640ea6457cf05487501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6054066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492743618ce250d8b5f53bf5f1e12404d57c3ec44625d5b44726e86f9bba5086`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f10f27efc9fb4dc2b4cdaada3f99aa2ffb9ebc99496fd55f1920263e51b914c9`  
		Last Modified: Thu, 14 Aug 2025 18:07:33 GMT  
		Size: 6.1 MB (6053556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bdfede140a8dbbb6956c184b88de98cc1662ecbef253a2a4433bc47021d07dc`  
		Last Modified: Thu, 14 Aug 2025 18:07:33 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:06dde395a53d1e08b8fd585a2037a3d0579d0cf26446b77df720fb5c757064f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b6f621ca40cc0a37945b871d68296b32cdb51732868485359bc907292b6eba`

```dockerfile
```

-	Layers:
	-	`sha256:6cffdd7549f5659166afe24fb85e23cfebf2409e108e1f347151569e8e28ba38`  
		Last Modified: Thu, 14 Aug 2025 20:56:30 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:815e928020aef447482878a6cef15fd72ac0f9d767b8309b032f7fb8feb7a353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6043424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbbf5945fb4360c4f621c54027b1cb47034cc2fa4d455ccc3f90923c1fe13761`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ba52e77e96ac90555714325e16a7b63d377c42dbeec68ba24cd503063cf7b9e0`  
		Last Modified: Thu, 14 Aug 2025 17:27:10 GMT  
		Size: 6.0 MB (6042914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ee5e05524b58d5802a62546f6f2347446d5321c4e8d583722db5b777d831d1`  
		Last Modified: Thu, 14 Aug 2025 17:27:08 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:842f4f4569460f34fc562978f687fc36581c388b02ab14cdad623893d588f5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2b1c717567f7faa2dde66fcb89acd6dcf382ec81408e1c26ecb2d68f03d105`

```dockerfile
```

-	Layers:
	-	`sha256:62da1307e4b0132c952bdd53d1b82eb3e96fa2934b1b582a8b7277351ddc31cd`  
		Last Modified: Thu, 14 Aug 2025 20:56:33 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d46af1d33927787659e676ea4714a6d53c8ba71956e0cda595d30ab277af5341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b7bb1d1d30e4a8233087664e0b5540f3e42f49f27589cfb43d23bacbeb63ffe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5823b59d47a0c660012e09655022b6660ce21c617ee2978f3edacb2ac344cb9f`  
		Last Modified: Thu, 14 Aug 2025 19:46:02 GMT  
		Size: 5.8 MB (5827281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e915dc222e2df5e58849a12f73e5fcede2bc08f2c98fd12f234ad34883849b`  
		Last Modified: Thu, 14 Aug 2025 19:46:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:4e9ff58758ddaea565568a15d4d049d69f51f01f69e9e0e517c68718dfe93ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a92dc3160475131a9aa4330ac0e14dedb97f5d4d57d5a386b4b1033afe203bc`

```dockerfile
```

-	Layers:
	-	`sha256:efd6b414c46e44a7c6cd8407e5887b4066f7e91785d16647bdfc24cb7dfb35a4`  
		Last Modified: Thu, 14 Aug 2025 20:56:36 GMT  
		Size: 10.6 KB (10649 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:70ad109d17470e9dbefe10df2ea372ea487e5a28cf96934110c5f6e6b118c4ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5807845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcf49d098aee252cf17a17945623b98c12312f01460230bd2494a20949c2703`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:221614c6b4427295323da315f973992219d61abd51aa73f549b80d617ceed783`  
		Last Modified: Thu, 14 Aug 2025 20:45:44 GMT  
		Size: 5.8 MB (5807337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea070ca5e9aa9e1edaa1764d931a0b0e385793e5b3124004b4ba91da5efc9e9`  
		Last Modified: Thu, 14 Aug 2025 20:45:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:bf4cec841a590e736bc48410cd41b4eb5176b07e39b161d5827a0dfe411fb72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd14ce8eff83929fceb915b93bd248d9837b402d7c289ab095bb35b5306608d`

```dockerfile
```

-	Layers:
	-	`sha256:f968b5bb7ad9cd95b31e5948c6d247e8ff2820fa830ca084746ac40f662b15d1`  
		Last Modified: Thu, 14 Aug 2025 23:56:26 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:66e24c97e22fd4db570efbde5c154dad761a934509688d1066ff6faf16c6ff8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6173621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5239fb0f4852c75ada10240d6ad54ccabbe1c300c54385271ab0d9c9a16d599`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 Aug 2025 12:51:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 Aug 2025 12:51:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 Aug 2025 12:51:02 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 Aug 2025 12:51:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 Aug 2025 12:51:02 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 Aug 2025 12:51:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:84a200250dfb971cfcf23197670e7ccfcfae55787bc8842c737081462376b978`  
		Last Modified: Mon, 04 Aug 2025 18:10:15 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5013d749e0797d9a012b7f969383e42b359cae57b7b1945f62eae07e6f12bbb`  
		Last Modified: Mon, 04 Aug 2025 18:10:15 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:3e90c2e5acc844d0189d6d664df76b3fc55d6438e1be7c1146763d00098ed8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469d8c0a969e19358745ad9513225279dd13b3d004003729b94ccd524773ffb5`

```dockerfile
```

-	Layers:
	-	`sha256:3490df75b7ac2f5425cf2a5decc578d60f595e9e0317faa4e73c20548b16f138`  
		Last Modified: Mon, 04 Aug 2025 20:56:51 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:nanoserver`

```console
$ docker pull nats@sha256:4b5bc1dda10956fffbd5637c74ca36f1f8e8999841816091381b80f7f4368b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:nanoserver` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:ad9de8f09f3634777b25adb56728db4ae6804eb3e93cf167d338af2569150272
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129178975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3e567374bac2065f94b8560a0f1747b427e881b5faa654919d1f7abccc554d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Thu, 14 Aug 2025 18:14:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 14 Aug 2025 18:14:05 GMT
RUN cmd /S /C #(nop) COPY file:3fa3039439cf4074860757aeaaa6c458fcb2a8fd53320637e2edb93570462bde in C:\nats-server.exe 
# Thu, 14 Aug 2025 18:14:06 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Aug 2025 18:14:07 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 14 Aug 2025 18:14:08 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Aug 2025 18:14:09 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70dd762bbc2519848d92e4250ffd2e8ad506e67e2ccc6edb8b28deb7bd6a4cc3`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8303cc1b67f588378cd15d48f0f9092ea5f9e1d8e2832d99a509bdd9c8ff70a`  
		Last Modified: Thu, 14 Aug 2025 18:14:54 GMT  
		Size: 6.5 MB (6512850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5204fc3573607851e777581d8f3393c06877a1b385138e9ddb562e41c44ae04f`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5811e67cadd8e8c18aa9f537c4147610482318cb56ca5e6a1ff3cff5d96e4cfc`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b880e68edcdaf39200bd33cc61fd60fab56c1eae85a872652a20730da3d12a`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbef80910535149a3762e6bfc014c51084a8c11fa366889b246185411c39fb9`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-ltsc2022`

```console
$ docker pull nats@sha256:4b5bc1dda10956fffbd5637c74ca36f1f8e8999841816091381b80f7f4368b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:ad9de8f09f3634777b25adb56728db4ae6804eb3e93cf167d338af2569150272
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129178975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3e567374bac2065f94b8560a0f1747b427e881b5faa654919d1f7abccc554d`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Thu, 14 Aug 2025 18:14:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 14 Aug 2025 18:14:05 GMT
RUN cmd /S /C #(nop) COPY file:3fa3039439cf4074860757aeaaa6c458fcb2a8fd53320637e2edb93570462bde in C:\nats-server.exe 
# Thu, 14 Aug 2025 18:14:06 GMT
RUN cmd /S /C #(nop) COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Aug 2025 18:14:07 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Thu, 14 Aug 2025 18:14:08 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Aug 2025 18:14:09 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70dd762bbc2519848d92e4250ffd2e8ad506e67e2ccc6edb8b28deb7bd6a4cc3`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8303cc1b67f588378cd15d48f0f9092ea5f9e1d8e2832d99a509bdd9c8ff70a`  
		Last Modified: Thu, 14 Aug 2025 18:14:54 GMT  
		Size: 6.5 MB (6512850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5204fc3573607851e777581d8f3393c06877a1b385138e9ddb562e41c44ae04f`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.7 KB (1674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5811e67cadd8e8c18aa9f537c4147610482318cb56ca5e6a1ff3cff5d96e4cfc`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b880e68edcdaf39200bd33cc61fd60fab56c1eae85a872652a20730da3d12a`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbef80910535149a3762e6bfc014c51084a8c11fa366889b246185411c39fb9`  
		Last Modified: Thu, 14 Aug 2025 18:14:53 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:afa7b504a629a7e9f8b4a3984a4dd796fe58a5267adbe0c18af723277657af7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:5634002bb5af84b0379f0de363bf0027b76bd6cf1a1db66ad254ae945a163cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6340078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d63b90f51c086da0db2adbc1a2ad7102ecabb8fa67c2470fdc2217b40a4d922`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b663fe8cd396789f2474139e39527f819c3a482db5e25e230cacaadd75df18ce`  
		Last Modified: Thu, 14 Aug 2025 17:27:46 GMT  
		Size: 6.3 MB (6339570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e38b65a6463af6a5ebdc0b02115f51a91399b2710a2758586bbeda7b6d50ba`  
		Last Modified: Thu, 14 Aug 2025 17:27:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:2ab05007143b6795815ff8714f15842e070df35013849973ca0b2f3552177ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310bb9bbe1f9febd06c494bb2dd5b961d7bf71acc8bf0b2fb53e0834a8cc2117`

```dockerfile
```

-	Layers:
	-	`sha256:85acdef1c273fe4667fee682e56c38f81137085631f156c2949814b3bc0d0bee`  
		Last Modified: Thu, 14 Aug 2025 20:56:26 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:40d95d59739fe46433103f4d262d1dd789f75ee44e99c640ea6457cf05487501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6054066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492743618ce250d8b5f53bf5f1e12404d57c3ec44625d5b44726e86f9bba5086`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f10f27efc9fb4dc2b4cdaada3f99aa2ffb9ebc99496fd55f1920263e51b914c9`  
		Last Modified: Thu, 14 Aug 2025 18:07:33 GMT  
		Size: 6.1 MB (6053556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bdfede140a8dbbb6956c184b88de98cc1662ecbef253a2a4433bc47021d07dc`  
		Last Modified: Thu, 14 Aug 2025 18:07:33 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:06dde395a53d1e08b8fd585a2037a3d0579d0cf26446b77df720fb5c757064f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b6f621ca40cc0a37945b871d68296b32cdb51732868485359bc907292b6eba`

```dockerfile
```

-	Layers:
	-	`sha256:6cffdd7549f5659166afe24fb85e23cfebf2409e108e1f347151569e8e28ba38`  
		Last Modified: Thu, 14 Aug 2025 20:56:30 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:815e928020aef447482878a6cef15fd72ac0f9d767b8309b032f7fb8feb7a353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6043424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbbf5945fb4360c4f621c54027b1cb47034cc2fa4d455ccc3f90923c1fe13761`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ba52e77e96ac90555714325e16a7b63d377c42dbeec68ba24cd503063cf7b9e0`  
		Last Modified: Thu, 14 Aug 2025 17:27:10 GMT  
		Size: 6.0 MB (6042914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ee5e05524b58d5802a62546f6f2347446d5321c4e8d583722db5b777d831d1`  
		Last Modified: Thu, 14 Aug 2025 17:27:08 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:842f4f4569460f34fc562978f687fc36581c388b02ab14cdad623893d588f5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2b1c717567f7faa2dde66fcb89acd6dcf382ec81408e1c26ecb2d68f03d105`

```dockerfile
```

-	Layers:
	-	`sha256:62da1307e4b0132c952bdd53d1b82eb3e96fa2934b1b582a8b7277351ddc31cd`  
		Last Modified: Thu, 14 Aug 2025 20:56:33 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d46af1d33927787659e676ea4714a6d53c8ba71956e0cda595d30ab277af5341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5827789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b7bb1d1d30e4a8233087664e0b5540f3e42f49f27589cfb43d23bacbeb63ffe`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5823b59d47a0c660012e09655022b6660ce21c617ee2978f3edacb2ac344cb9f`  
		Last Modified: Thu, 14 Aug 2025 19:46:02 GMT  
		Size: 5.8 MB (5827281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e915dc222e2df5e58849a12f73e5fcede2bc08f2c98fd12f234ad34883849b`  
		Last Modified: Thu, 14 Aug 2025 19:46:01 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:4e9ff58758ddaea565568a15d4d049d69f51f01f69e9e0e517c68718dfe93ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a92dc3160475131a9aa4330ac0e14dedb97f5d4d57d5a386b4b1033afe203bc`

```dockerfile
```

-	Layers:
	-	`sha256:efd6b414c46e44a7c6cd8407e5887b4066f7e91785d16647bdfc24cb7dfb35a4`  
		Last Modified: Thu, 14 Aug 2025 20:56:36 GMT  
		Size: 10.6 KB (10649 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:70ad109d17470e9dbefe10df2ea372ea487e5a28cf96934110c5f6e6b118c4ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5807845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcf49d098aee252cf17a17945623b98c12312f01460230bd2494a20949c2703`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 14 Aug 2025 15:30:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 14 Aug 2025 15:30:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 14 Aug 2025 15:30:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 14 Aug 2025 15:30:07 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 14 Aug 2025 15:30:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:221614c6b4427295323da315f973992219d61abd51aa73f549b80d617ceed783`  
		Last Modified: Thu, 14 Aug 2025 20:45:44 GMT  
		Size: 5.8 MB (5807337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea070ca5e9aa9e1edaa1764d931a0b0e385793e5b3124004b4ba91da5efc9e9`  
		Last Modified: Thu, 14 Aug 2025 20:45:40 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:bf4cec841a590e736bc48410cd41b4eb5176b07e39b161d5827a0dfe411fb72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd14ce8eff83929fceb915b93bd248d9837b402d7c289ab095bb35b5306608d`

```dockerfile
```

-	Layers:
	-	`sha256:f968b5bb7ad9cd95b31e5948c6d247e8ff2820fa830ca084746ac40f662b15d1`  
		Last Modified: Thu, 14 Aug 2025 23:56:26 GMT  
		Size: 10.6 KB (10556 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:scratch` - linux; s390x

```console
$ docker pull nats@sha256:66e24c97e22fd4db570efbde5c154dad761a934509688d1066ff6faf16c6ff8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6173621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5239fb0f4852c75ada10240d6ad54ccabbe1c300c54385271ab0d9c9a16d599`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 01 Aug 2025 12:51:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Fri, 01 Aug 2025 12:51:02 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Fri, 01 Aug 2025 12:51:02 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Fri, 01 Aug 2025 12:51:02 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Fri, 01 Aug 2025 12:51:02 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 01 Aug 2025 12:51:02 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:84a200250dfb971cfcf23197670e7ccfcfae55787bc8842c737081462376b978`  
		Last Modified: Mon, 04 Aug 2025 18:10:15 GMT  
		Size: 6.2 MB (6173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5013d749e0797d9a012b7f969383e42b359cae57b7b1945f62eae07e6f12bbb`  
		Last Modified: Mon, 04 Aug 2025 18:10:15 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:scratch` - unknown; unknown

```console
$ docker pull nats@sha256:3e90c2e5acc844d0189d6d664df76b3fc55d6438e1be7c1146763d00098ed8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469d8c0a969e19358745ad9513225279dd13b3d004003729b94ccd524773ffb5`

```dockerfile
```

-	Layers:
	-	`sha256:3490df75b7ac2f5425cf2a5decc578d60f595e9e0317faa4e73c20548b16f138`  
		Last Modified: Mon, 04 Aug 2025 20:56:51 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:cd40ad4037d8bcb19778d0ec3407978059ea88d895747dfce3ea1be3f83f5760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:ff0d0047ceb610a0b73edcb6d12305bdf06e08a127258cf923e1aec9645ec419
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2288892735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe5b93e3cd45a63955014ff0d53cf5383f91b868d6bacf1c242ce4861d0a3fe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Thu, 14 Aug 2025 17:24:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 14 Aug 2025 17:24:18 GMT
ENV NATS_DOCKERIZED=1
# Thu, 14 Aug 2025 17:24:19 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 17:24:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.8/nats-server-v2.11.8-windows-amd64.zip
# Thu, 14 Aug 2025 17:24:21 GMT
ENV NATS_SERVER_SHASUM=3dd98465626e8c6ed92a784ef13c3f956c7e87fbbb4ee86cc198e377565eaeaf
# Thu, 14 Aug 2025 17:24:28 GMT
RUN Set-PSDebug -Trace 2
# Thu, 14 Aug 2025 17:24:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 14 Aug 2025 17:24:44 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Aug 2025 17:24:45 GMT
EXPOSE 4222 6222 8222
# Thu, 14 Aug 2025 17:24:46 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Aug 2025 17:24:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3f006d1cb294833347c0dcdeff82dda52af9acbea696337fd8408869317713`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e0fe1f9e451f5b78de6f2eabbcf9dd583e44cc8efca284c024e6fc31fea206`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4c9efb293cf4538944d58d49d978df5a06ed2586f43c0312291c6ed0854b98`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4fcdec518a7d5e9cbdbb2398711d526df04c6abd46f6dc74c91ce20cb62a28`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f32d8dbe729b86cde1eafd2da61359f32dab9aa4ff767aa70b3dc9351ba01c3`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1453289e44dd8e7a29b2a8395640bb6a2e2ebd47060a6bfe129031ce2072d7`  
		Last Modified: Thu, 14 Aug 2025 17:26:08 GMT  
		Size: 336.2 KB (336246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db38558f3d85860c055f99e79e865d42a17dd691a4f83ea93e0f8a5e391d125`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 6.9 MB (6852407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb87097b18d82c7dc42b80c5f6912e34cd08ecb316ffd445266fbb02ee18352b`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828b5772011538e3bb3bd9055b2b9e9b10bb6ffd46dc54a1d765d3e2dcfb03a6`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd3abb758a5b3c339001a04d7364df2b54b00e27711aecf5f44a76323ef676f`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366367ce039c79734b9ad15e13867ea0fd5f18ee46cc185dde59b3507a9b3392`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-ltsc2022`

```console
$ docker pull nats@sha256:cd40ad4037d8bcb19778d0ec3407978059ea88d895747dfce3ea1be3f83f5760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `nats:windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull nats@sha256:ff0d0047ceb610a0b73edcb6d12305bdf06e08a127258cf923e1aec9645ec419
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2288892735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe5b93e3cd45a63955014ff0d53cf5383f91b868d6bacf1c242ce4861d0a3fe`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Thu, 14 Aug 2025 17:24:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 14 Aug 2025 17:24:18 GMT
ENV NATS_DOCKERIZED=1
# Thu, 14 Aug 2025 17:24:19 GMT
ENV NATS_SERVER=2.11.8
# Thu, 14 Aug 2025 17:24:20 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.11.8/nats-server-v2.11.8-windows-amd64.zip
# Thu, 14 Aug 2025 17:24:21 GMT
ENV NATS_SERVER_SHASUM=3dd98465626e8c6ed92a784ef13c3f956c7e87fbbb4ee86cc198e377565eaeaf
# Thu, 14 Aug 2025 17:24:28 GMT
RUN Set-PSDebug -Trace 2
# Thu, 14 Aug 2025 17:24:43 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Thu, 14 Aug 2025 17:24:44 GMT
COPY file:b1a2608448de8d5c0c689957fe95cded96220a69167c54a1ee78e8da625c6311 in C:\nats-server.conf 
# Thu, 14 Aug 2025 17:24:45 GMT
EXPOSE 4222 6222 8222
# Thu, 14 Aug 2025 17:24:46 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Thu, 14 Aug 2025 17:24:47 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3f006d1cb294833347c0dcdeff82dda52af9acbea696337fd8408869317713`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e0fe1f9e451f5b78de6f2eabbcf9dd583e44cc8efca284c024e6fc31fea206`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4c9efb293cf4538944d58d49d978df5a06ed2586f43c0312291c6ed0854b98`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4fcdec518a7d5e9cbdbb2398711d526df04c6abd46f6dc74c91ce20cb62a28`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f32d8dbe729b86cde1eafd2da61359f32dab9aa4ff767aa70b3dc9351ba01c3`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1453289e44dd8e7a29b2a8395640bb6a2e2ebd47060a6bfe129031ce2072d7`  
		Last Modified: Thu, 14 Aug 2025 17:26:08 GMT  
		Size: 336.2 KB (336246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db38558f3d85860c055f99e79e865d42a17dd691a4f83ea93e0f8a5e391d125`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 6.9 MB (6852407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb87097b18d82c7dc42b80c5f6912e34cd08ecb316ffd445266fbb02ee18352b`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828b5772011538e3bb3bd9055b2b9e9b10bb6ffd46dc54a1d765d3e2dcfb03a6`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd3abb758a5b3c339001a04d7364df2b54b00e27711aecf5f44a76323ef676f`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366367ce039c79734b9ad15e13867ea0fd5f18ee46cc185dde59b3507a9b3392`  
		Last Modified: Thu, 14 Aug 2025 17:26:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
