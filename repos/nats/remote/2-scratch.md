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
