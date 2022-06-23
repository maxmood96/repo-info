## `debian:oldoldstable-backports`

```console
$ docker pull debian@sha256:ee77c8f68d431fb6e6c294ae0bcca7c4fc9c6502aa64fbfd7b9bdfd95b4f4df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldoldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:8dd0167ccdd2371ca882baf98d2b13d5fb660677642f8037e8ae1fd4fd7da673
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45430233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7369d7f5b376467e06b11a80f11356be076a1dd34eac011c6561f596b2e57e8b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:54 GMT
ADD file:c5c0a879b9cc71570f7f73c32f60c1f5c4d67ffdfb76b93e1eb165e04963bb83 in / 
# Thu, 23 Jun 2022 00:20:55 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:20:59 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8a1ffd64e351e740ee3062f524c2645ff4711d85bf3b9b3d5fea2041844d0b12`  
		Last Modified: Thu, 23 Jun 2022 00:26:23 GMT  
		Size: 45.4 MB (45430007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06187aaa1cb148a468fbd1478b551c7ab25da59e18d4a2eeba9e9709265045e9`  
		Last Modified: Thu, 23 Jun 2022 00:26:32 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:2f3e7d2838f980520eb3dd856fac1ad085441fa96164893a41523428390b000c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44124913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a63af2a74894aeadf4f1d9e2010aed520d11d7b67d3d0cc3122750a2f74402e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:52:05 GMT
ADD file:98f8fb6bc22230e75ea11093c43e34d7ae2c0588355847345191e3ce4a914f75 in / 
# Thu, 23 Jun 2022 00:52:06 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:52:18 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:d6ca348fb810689565ac791729c8d5e90b0e3a12ade298b5284944e463950525`  
		Last Modified: Thu, 23 Jun 2022 01:07:55 GMT  
		Size: 44.1 MB (44124687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68db3a58b118aa92a6a4ab3708d572e852fa420cbd9bf4306d932a5ef9011486`  
		Last Modified: Thu, 23 Jun 2022 01:08:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:4e8bf1ff4eb58be2d62db3463986378e1fe96277dac62d51319b3e150025fa6e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42151075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8e744cf09d3ae1ab2ea28dbf191df96656e0ef7120814eafc0d8cd2b681bcc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:01:17 GMT
ADD file:69e8ef513dcbb145d5981d8a65edd287ea77f2c6b386c5cd41a1f848ec3228b1 in / 
# Thu, 23 Jun 2022 01:01:18 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:01:31 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a3a023022ab10d4a4c483831282abe847b57d8ec712684b55417cb697d877750`  
		Last Modified: Thu, 23 Jun 2022 01:17:32 GMT  
		Size: 42.2 MB (42150849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f672dd0261a642b20015195d1727c9863eba229136d6944a82c5e56bb75958a`  
		Last Modified: Thu, 23 Jun 2022 01:17:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:3d043ed6cd8ebc26b31b9918dfcaa7d4b7c2f3c51374664df0e16f728a599e9e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43213347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82bb0e1edacd0678b244061dff305518e5d1d61f1aee7b415133ee8949a25cb2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:18 GMT
ADD file:586acde5ce950f9b9e13f16f75f04e78c34054315d9caeb76761fb3dda128422 in / 
# Thu, 23 Jun 2022 00:41:20 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:41:25 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8fbc388e06ada1118e1a0453990691abaa76135b62954233bbb8100eabd84dce`  
		Last Modified: Thu, 23 Jun 2022 00:48:38 GMT  
		Size: 43.2 MB (43213118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d29508ac610e4f3889fbe301c539438a34375db315144c5571fe26e7f1e62a`  
		Last Modified: Thu, 23 Jun 2022 00:48:49 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldoldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:b711c60f9382dd34edfb5230029d76649a8838cbe59d20a13ee555c8f25b209f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46150821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56e5aadcd1f4cc8474a7b197311f403eebd07680aad5ac74003ed35db7b56e6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:40:11 GMT
ADD file:52342a932fbf8e83041a91d59b6a769fc82e041a08d6ab6ecea38a77830ad4f7 in / 
# Thu, 23 Jun 2022 00:40:11 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:40:17 GMT
RUN echo 'deb http://deb.debian.org/debian oldoldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7140bd4d5ac5543b07c6f0601591e8e9b224be93975dda5a8a7ac8683104b23c`  
		Last Modified: Thu, 23 Jun 2022 00:48:03 GMT  
		Size: 46.2 MB (46150594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed3b002df9f056513da2446e08a65d4b7f55509f8f13523a46e91f30502ffac5`  
		Last Modified: Thu, 23 Jun 2022 00:48:15 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
