## `alt:sisyphus`

```console
$ docker pull alt@sha256:fd749c14bcd6f85bc5bad4d63fa6c593ea29905e297abcb55b5c365b5a7410a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `alt:sisyphus` - linux; amd64

```console
$ docker pull alt@sha256:0bb07859639e226337aaf22bc8b293d79d170054d3b902ffb45c6a23001bf7e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42190568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d051b620ce6b5d039d249bd0ffe717809be04fc4936c7c7381356a020625267`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 04 Aug 2021 22:28:37 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Mar 2024 00:35:00 GMT
ADD file:59d874d2e1cbfacc14696915b0d10b77fa761491452b8b7332bd8344e13832c8 in / 
# Tue, 26 Mar 2024 00:35:01 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Mar 2024 00:35:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e92e2a59e32fb52c3c83bbd2f579d708bba44c585a2040277eb38bd3d74a2340`  
		Last Modified: Tue, 26 Mar 2024 00:35:32 GMT  
		Size: 42.2 MB (42190377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0185efb53c2a20a12339ee5c0df91560e00533bdae3d97ff827430bc71202579`  
		Last Modified: Tue, 26 Mar 2024 00:35:25 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:sisyphus` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:84728c610032152137915d52536da0b03c3d99ab83853d9efef2749fa876f753
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (40999397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c58c7ab0dc86b582fddbf456eef18c05812b43d2d0828aa026d86b8a1e90a393`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:39:36 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Mar 2024 00:27:44 GMT
ADD file:b726b3f38b840775128aca0361fa2d16d662710d2e5144bbfa3d6477b57c9d6e in / 
# Tue, 26 Mar 2024 00:27:45 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Mar 2024 00:27:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ae0204cee66384724a36827a5d0e71933ed4b89470905532630fead17af75204`  
		Last Modified: Tue, 26 Mar 2024 00:28:13 GMT  
		Size: 41.0 MB (40999205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81c43f59c9c5296f22a87148501ec55fd4cbeb41baee2b53ced5ba9945a6ec9`  
		Last Modified: Tue, 26 Mar 2024 00:28:08 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:sisyphus` - linux; 386

```console
$ docker pull alt@sha256:c366a71922398907e0ab02f26f39b0fa4342717479967c2ac6d64aa1f6f8e4bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42330009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1ea1c88c71fe1278cf31d65763bb1aa6531c1d62ab6789c7fca7b742bc0806`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Jul 2023 23:38:46 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Mar 2024 01:00:13 GMT
ADD file:0b365b70061f0a638d24b52f6a5cf6de460d3c0361d4b8a653fe21c42f92f46f in / 
# Tue, 26 Mar 2024 01:00:14 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Mar 2024 01:00:14 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b895f6cc6490b4c7324f648bc3e02f7def799d31e26454588f22b68383681bd3`  
		Last Modified: Tue, 26 Mar 2024 01:00:51 GMT  
		Size: 42.3 MB (42329819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b71ceec1145e7f71adc79fed3272948bfaff4d6c77ae8a2cdc2595700a039b`  
		Last Modified: Tue, 26 Mar 2024 01:00:42 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `alt:sisyphus` - linux; ppc64le

```console
$ docker pull alt@sha256:133619f2b08779fdb3d1a3c085a8823646940fd4a01023880e86d332cd6c9d95
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44451882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843a0c05676c605d455a9cd00deca8c1cf41a2a4bec14a300c90dcc9fd508625`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:16:44 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Tue, 26 Mar 2024 00:18:53 GMT
ADD file:53af9cc2d9792fbc30ab3bb757b1e7554a8c9e176ac506e30623944aab59670e in / 
# Tue, 26 Mar 2024 00:19:10 GMT
RUN true > /etc/security/limits.d/50-defaults.conf
# Tue, 26 Mar 2024 00:19:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:93301f406215feca246cf97ed1854abe85a246980fb5893137bb0a7e1da40a8c`  
		Last Modified: Tue, 26 Mar 2024 00:19:48 GMT  
		Size: 44.5 MB (44451691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e54f39ecf389639638882b96fdb17664956e2792039ba2449040d1e78f4efd`  
		Last Modified: Tue, 26 Mar 2024 00:19:41 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
