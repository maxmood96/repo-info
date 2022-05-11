## `debian:stretch-backports`

```console
$ docker pull debian@sha256:821e35feeb233d42361963ad67f5b09677468895c44389f7403cf826b4025a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:stretch-backports` - linux; amd64

```console
$ docker pull debian@sha256:57fc99afb64bf557f291af722f6f35dd6a37bc86a1b0dda7b424ce7830f634df
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45428230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f09cabe5e0be350dc1bad9eb36245d644136dc65cb38438a4cce3e7cd469c93`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:22:05 GMT
ADD file:00f57642edc8479d50e6470a3509ad679eb9353761912deade33251fb3d9daa8 in / 
# Wed, 11 May 2022 01:22:05 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:22:08 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:06e39e28714dba08fe310ca1aafb43905427729ecf8e9586f811a7e5062fd09b`  
		Last Modified: Wed, 11 May 2022 01:28:34 GMT  
		Size: 45.4 MB (45428005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4b733396f7f38f2e0c9fd6fc52c9bf60108d00707f614c5da12f3557c2de71`  
		Last Modified: Wed, 11 May 2022 01:28:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:fb1c1235d76db690bb01da68e0402ca5d2c1ed4d111f797b75060437b46dc8a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44123080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:715afcefe509b51f1e36c84c71c4a541020ec08dadc41a8f6e96a95229aa69d2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:55:33 GMT
ADD file:95b054735b431afab54d50818bab5058e711871345ec62ca3036290e76c5002c in / 
# Wed, 11 May 2022 00:55:34 GMT
CMD ["bash"]
# Wed, 11 May 2022 00:55:49 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:342be1c547ac3ac45aaed473477b6660f99f4de775e90a96d72de9ed5e557bd3`  
		Last Modified: Wed, 11 May 2022 01:13:02 GMT  
		Size: 44.1 MB (44122855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ac31a33faf1aa82d100c86ae2e3d30c0445c941b3e76de60751dd34a71f405`  
		Last Modified: Wed, 11 May 2022 01:13:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:387a9ce9b72ec1a85f0b7de1d3f54b255b44f3ff18a35deb5f8af2d3f287371f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42151387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e5434211153bc427d178be1318418e2252a3fa02d07d50fbd248521a0cda92`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:54:33 GMT
ADD file:c679388ac7a37037465302aea3117354d9746d0c50c056e826b5c8c58aea5138 in / 
# Wed, 11 May 2022 01:54:34 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:54:49 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:629c5b996bdb9cea71f1d194d7a244d4aba271133bad4f5b88bfe38c4626349a`  
		Last Modified: Wed, 11 May 2022 02:11:17 GMT  
		Size: 42.2 MB (42151163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d056a5c8cade331b4a1c18ff0ff4ec0777b13efe734adb72558eb41b5a2c1112`  
		Last Modified: Wed, 11 May 2022 02:11:37 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:8e23dc798a278d4b9fc5cfc8842fb969d7f76bb23881dbb4c14ce98622f67596
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43212700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a78d3d56827c40d7e4cc3bd00933e8c7b34f6932b9efb3d74006112df4f4dbbd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:49:08 GMT
ADD file:8949016fba61b18207f5a2309fc974562080c5cc80d1eb82adb35c4fa03f6f05 in / 
# Wed, 11 May 2022 00:49:09 GMT
CMD ["bash"]
# Wed, 11 May 2022 00:49:16 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:139065d8f4553df403babda56f830c32aa1f3e57f18d2145a3179468921a4bb8`  
		Last Modified: Wed, 11 May 2022 00:57:26 GMT  
		Size: 43.2 MB (43212478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff4b987e4f9e991115fa22560396509e47c43c1fa2320752637f535a9dfe859`  
		Last Modified: Wed, 11 May 2022 00:57:43 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; 386

```console
$ docker pull debian@sha256:eed9d52e7017b24903544c8b53e617ee1d25a26c9e92c067986746e1affb79ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46148470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32686d7a24d0ea717d1b6f921220f93462a83b58871f62e4a00678f48f9c1539`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:41:29 GMT
ADD file:613b0ab502f24046bdd1e70cebcb6d532bab2f5e1a0c6bdcc47f6a60ce1726b5 in / 
# Wed, 11 May 2022 01:41:30 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:41:37 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7d1fe5ccfab549c84b336904d14cd0e82b58e9cb11a2fa8356d34934aa7f8a39`  
		Last Modified: Wed, 11 May 2022 01:50:24 GMT  
		Size: 46.1 MB (46148247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26415a5d2c4394bdbc38c605e67cf5a9578e9b6190a27524db4fa2ba7d7ecebb`  
		Last Modified: Wed, 11 May 2022 01:50:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
