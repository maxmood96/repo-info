## `oraclelinux:9-slim-fips`

```console
$ docker pull oraclelinux@sha256:035f56dbe7ef71c41351d313d7efba85c2329f94e6693ad1a43e31dc85cd57bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `oraclelinux:9-slim-fips` - linux; amd64

```console
$ docker pull oraclelinux@sha256:9f2d01efabdded5aded68e189150477945afb1f58ab44ceb9dc674555b6c330c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49257016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdc0b63d38dbd02f5ff971af479e66f1615210582df66924eb0b85f9c55558f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 09 Sep 2024 20:34:59 GMT
ADD oraclelinux-9-slim-fips-amd64-rootfs.tar.xz / # buildkit
# Mon, 09 Sep 2024 20:34:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0f2eae4f5eba29dfe91172d0168536e3c9405042e291668410df25662b898fb1`  
		Last Modified: Tue, 10 Sep 2024 01:03:55 GMT  
		Size: 49.3 MB (49257016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `oraclelinux:9-slim-fips` - unknown; unknown

```console
$ docker pull oraclelinux@sha256:360b468929aeaf5ddcc6af3fba33c72801889d933d760b4874d8e963d899ea5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2193870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce066d466c7ffb3c6d76f9c0216ae9ca522281f9c26cc95e32724304cfc3743d`

```dockerfile
```

-	Layers:
	-	`sha256:2ff3ce65dfa7729c44e1cb640999fb1a418f89ba2e9f383e9416ce0ba0947c63`  
		Last Modified: Tue, 10 Sep 2024 01:03:54 GMT  
		Size: 2.2 MB (2188985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3f0589b5d2ee19bb0c126a4e1dbcde1b935d4bd03e710788aa5ba0943583c70`  
		Last Modified: Tue, 10 Sep 2024 01:03:53 GMT  
		Size: 4.9 KB (4885 bytes)  
		MIME: application/vnd.in-toto+json

### `oraclelinux:9-slim-fips` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:7ed502087552a654d503e686fdffbe47764ceb58395c70907efe2d24d8477dcc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47913413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7282a89d905be8e9d95bba152e67fa043edec33498fb003af7f28d455d0e9189`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 09 Sep 2024 21:41:26 GMT
ADD file:253fccb2492f79bb0d92559f76b4c86362e111c5a154a121d51b9a14e6b224cd in / 
# Mon, 09 Sep 2024 21:41:27 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2325c1a563ebb9b603d9c9d1ad22a9a344af21887da101f3aef0c51d4ce8b0f8`  
		Last Modified: Mon, 09 Sep 2024 21:42:26 GMT  
		Size: 47.9 MB (47913413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
