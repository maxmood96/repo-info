## `registry:latest`

```console
$ docker pull registry@sha256:5bb9b919833aa955dfe1d1121cc038330b025ec6506ce47066c9192927e3dc3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `registry:latest` - linux; amd64

```console
$ docker pull registry@sha256:160c621b9bd98c4becce1c3b14e4866524dbe898d3af2e48d81fa1821b82c615
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9939523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee34aa9d8ab2cac40f256d19556838868d34bf80ad0857aa4a9501a4d1359ac6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:19 GMT
ADD file:c744c1dc3da4145771e66d90e2e97a4f7fb702e5e07cf4e766ee0792cf161d92 in / 
# Wed, 31 Mar 2021 20:10:19 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 17:27:32 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Thu, 01 Apr 2021 17:27:33 GMT
COPY file:21256ff7df5369f7ad2e19c6d020a644303aded200bdbec4d46648f38d55df78 in /bin/registry 
# Thu, 01 Apr 2021 17:27:33 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 01 Apr 2021 17:27:33 GMT
VOLUME [/var/lib/registry]
# Thu, 01 Apr 2021 17:27:33 GMT
EXPOSE 5000
# Thu, 01 Apr 2021 17:27:34 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 01 Apr 2021 17:27:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Apr 2021 17:27:34 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:9b794450f7b6db7c944ba1f4161edb68cb535052fe7db8ac06e613516c4a658d`  
		Last Modified: Wed, 31 Mar 2021 20:11:14 GMT  
		Size: 2.8 MB (2815346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba25693af03cb1f1c7465cc7725fe84b1ad480bed32cf5e7df2fd41ecd3ea57`  
		Last Modified: Thu, 01 Apr 2021 17:27:46 GMT  
		Size: 299.6 KB (299641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb68e7589ff7cf1ca88439ca967f28e9df091bcd06452b8dfa96c7cef6d6541`  
		Last Modified: Thu, 01 Apr 2021 17:27:46 GMT  
		Size: 6.8 MB (6823926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf77150f6657b941e820089c52e1ebc7171a82efd8b5552d10afe7bdc341e43`  
		Last Modified: Thu, 01 Apr 2021 17:27:45 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339e0c26c7cc61c989502122271496b526a44ed34cf799b7862a5d35d6ac35a2`  
		Last Modified: Thu, 01 Apr 2021 17:27:45 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm variant v6

```console
$ docker pull registry@sha256:82b4ae365aa03c555c6ec69e2fe60964b829a9252775a487fbceabc2d49bcca4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db2d18a4dc279a653234ceb0c949c45dbb152c956023d679d94b2fddf188b75`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 31 Mar 2021 17:19:20 GMT
ADD file:15a1f9d3700deb648f0b3701afebc97ff28eb30d1b55e18dc9c696a9dd5c8e36 in / 
# Wed, 31 Mar 2021 17:19:21 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 03:03:13 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Thu, 01 Apr 2021 03:03:15 GMT
COPY file:29c6c1625420a558a03cc7ed253192f8138cba6212b64e30217fb6488af668e2 in /bin/registry 
# Thu, 01 Apr 2021 03:03:16 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 01 Apr 2021 03:03:17 GMT
VOLUME [/var/lib/registry]
# Thu, 01 Apr 2021 03:03:18 GMT
EXPOSE 5000
# Thu, 01 Apr 2021 03:03:19 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 01 Apr 2021 03:03:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Apr 2021 03:03:21 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:ac95243af174972febc49043f62f7b952a0c610e59b55ac4133f442e399e8729`  
		Last Modified: Wed, 31 Mar 2021 17:20:17 GMT  
		Size: 2.6 MB (2621248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81abd9ad682b4554d8eef9a3e45d373886c1e3aa52c33febc1fb42c1a41099e3`  
		Last Modified: Thu, 01 Apr 2021 03:03:38 GMT  
		Size: 299.9 KB (299934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c16d1e58d4635a248334fe48ce9dc26dbddd3b86b905b2c0375ddd11aa24ef`  
		Last Modified: Thu, 01 Apr 2021 03:03:40 GMT  
		Size: 6.4 MB (6391088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2d3d6fc8a860cb1c030a937de0e4330791152d68acfa11aff172fc74d6b1500`  
		Last Modified: Thu, 01 Apr 2021 03:03:38 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1a5d247010eed566ec69e2a0949843b89441c5b0128383c1e699ee07cf1434`  
		Last Modified: Thu, 01 Apr 2021 03:03:38 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `registry:latest` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:cbbc47a2e4d7b278b41e1d93550f86990bca63cf0ffad039bded132d9de8804c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9266755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1610c492cc33547f8f05283198ca54dfe2f6f1b1ecf7274aa6f1e05071f580`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Wed, 31 Mar 2021 17:22:02 GMT
ADD file:174ba1b913c5cf549fcdfc259e8e3aa8f49cea660865fd54b8aacb430602a783 in / 
# Wed, 31 Mar 2021 17:22:03 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 16:13:52 GMT
RUN set -ex     && apk add --no-cache ca-certificates
# Thu, 01 Apr 2021 16:13:53 GMT
COPY file:51a441e6eceff49ef32609e7070b64e8d5690648e4f915cc825274e6fe37aed2 in /bin/registry 
# Thu, 01 Apr 2021 16:13:55 GMT
COPY file:4544cc1555469403b322faecc1cf1ca584667c43a6a60b17300f97840c04196e in /etc/docker/registry/config.yml 
# Thu, 01 Apr 2021 16:13:56 GMT
VOLUME [/var/lib/registry]
# Thu, 01 Apr 2021 16:13:57 GMT
EXPOSE 5000
# Thu, 01 Apr 2021 16:13:58 GMT
COPY file:507caa54f88c1f3862e5876e09a108b2083630ba24c57ad124e356a2de861d62 in /entrypoint.sh 
# Thu, 01 Apr 2021 16:13:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 01 Apr 2021 16:14:00 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:a3cf95b55367cb73f51318ee9c854def347373482336709ca1882a5d4c20b7c7`  
		Last Modified: Wed, 31 Mar 2021 17:23:00 GMT  
		Size: 2.7 MB (2725871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb20fb27eaf196c6624e401920fa255ca523639d655ecf44cdc50a850d1dcae1`  
		Last Modified: Thu, 01 Apr 2021 16:14:16 GMT  
		Size: 300.1 KB (300071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6529d4952e72f2b79319a563c16a6366aece654e007ed54215dd9a9be6e6b3`  
		Last Modified: Thu, 01 Apr 2021 16:14:16 GMT  
		Size: 6.2 MB (6240200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0b4520f23f0e299ca480c6bb07fc6d312c880df74db632ff0d77d209a93da6`  
		Last Modified: Thu, 01 Apr 2021 16:14:14 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67d9d0b88391c0f1670f2066dc4c52ff97b9198fd364ac7a4f0338e0cdcb996`  
		Last Modified: Thu, 01 Apr 2021 16:14:15 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
