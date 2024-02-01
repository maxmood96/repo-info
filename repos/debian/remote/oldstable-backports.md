## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:58e105ec20080afdb05cd496c5e25e6795b67b8034ca406faf23d7ee4323be1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:af0df2ea4372b90461ebf6fb59d2d090f3439e6c193659e8ea61ba97480da3c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55057185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0a587eb3f75f267ba1335f500af46ca535ea8423fe512d1fc651603b54cffd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:36:35 GMT
ADD file:58599727624acb0fd6e3a9b4cf5d32db224174bf0fbcac80eda8cab0f28bf461 in / 
# Wed, 31 Jan 2024 22:36:35 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:36:39 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0ee9f016f35b531313ea70b99cf50f3289e16243a11ceb7d4474db3ffc474f37`  
		Last Modified: Wed, 31 Jan 2024 22:42:25 GMT  
		Size: 55.1 MB (55056962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9923d33383a3b1b29a323d7a9edaa4f8ccb1c22b2acc1aaa9cd71b0e5265556a`  
		Last Modified: Wed, 31 Jan 2024 22:42:34 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:9102135b7977f12b023858beb6adb6d543c3b150b106e98389f7791daa20eb9b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52561110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa45919e0390a12b704752986203ed0c426dbac014fd4c4a632cc15e8367ddaa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:50 GMT
ADD file:2d4909e4471b29427bec8738b53173e4b002291f253ead272ca4ce33d80436f3 in / 
# Wed, 31 Jan 2024 22:44:54 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:44:57 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:54e04fda41c9aa098e303e8b39eebf475b35f694a66264c615fedee3f63eb0ac`  
		Last Modified: Wed, 31 Jan 2024 22:49:10 GMT  
		Size: 52.6 MB (52560883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ccfefd478d733dbe4e5b731e2db20b84d1b30814f63a3f59735fff0292ed6e0`  
		Last Modified: Wed, 31 Jan 2024 22:49:19 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:cb78cc04b45611f3693f2c2ed2db379f02feb88802fb37490b47aac6cde4ce07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50216445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0526601a691f87aaa863df6b6fc5e3f9fa4e4503522a194388ce096e105c1969`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:35 GMT
ADD file:e874658ff20443546507b3272cdf36c55906a84b30dc6687c6071b0b82c2e8c6 in / 
# Wed, 31 Jan 2024 22:45:35 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:45:39 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9dad99aab5198769ad94b3a25c52746482d6bbf15c0f01149cfc1a2e60146a7f`  
		Last Modified: Wed, 31 Jan 2024 22:51:15 GMT  
		Size: 50.2 MB (50216219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92789ed4aced2af3ad82397f3815d2cc8ea2f47d8023953d85460857fd03805`  
		Last Modified: Wed, 31 Jan 2024 22:51:24 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:479df0e937dfd3e6c4c9e1dc213c22e96067543dc7e1fce37a653481b3d052e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53708491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fadef6048bc0d6a9b5187a665d7843206cd3744855f522936d2655fb04bd185`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:45:19 GMT
ADD file:e95d3eb89eb9c6cfd01900362d980e8bae72b9512a712b2643b1055d877caa62 in / 
# Wed, 31 Jan 2024 22:45:20 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:45:23 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0632c4ad398d72b44c05cbe440314af40005058cd68457214dddeb7316883700`  
		Last Modified: Wed, 31 Jan 2024 22:50:28 GMT  
		Size: 53.7 MB (53708267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6947c1a3f164051503d9abf9c08b90e729cb3d9d03ae55af2ff4db924429a112`  
		Last Modified: Wed, 31 Jan 2024 22:50:37 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:3ee917dc71418374bd14e7882003456b00ed69846ca29bb8f2dcab435d73d1ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56046552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131a897034cabe34a17f7bccdd49fb61f7379c49adcfd665a919030c0fc1548f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:40:18 GMT
ADD file:07c2063ad30bb35a2e77ae5d718a1eeae21a1f539e878c1175dfd85480c6da26 in / 
# Wed, 31 Jan 2024 22:40:18 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:40:21 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:29e798a669c30d3eadb4ebdf470280f88c8a41e1bf0becba88cb9eafc8c10c69`  
		Last Modified: Wed, 31 Jan 2024 22:46:28 GMT  
		Size: 56.0 MB (56046326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b49a2730edf529995d8196f539e4396b751dce1320ed6da9da9841043458010`  
		Last Modified: Wed, 31 Jan 2024 22:46:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:94c32d59b0a420b39f44b69b27960304657df29609044e1acec49a375b587609
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53289324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad63a5e7b024502c300e4de2b0e4605bc786356366f68bb7c7ec056ac2599027`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:29:04 GMT
ADD file:5d629b85aff113f4061d5c2082b41bbf522051504f0ec536edfbb3cf289bb29c in / 
# Wed, 31 Jan 2024 22:29:10 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:29:25 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:010963cca2dc7d83d9ca301dc0979f56fb08edea6b55b03c0501c1e11dc94bf6`  
		Last Modified: Wed, 31 Jan 2024 22:40:30 GMT  
		Size: 53.3 MB (53289095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4cd90078adc0d9dbf5d8daa7544f3e5fcd741486d3ec084f309025b2ab33f15`  
		Last Modified: Wed, 31 Jan 2024 22:40:41 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:5cfe7276154fafaec845e005392ee7a0b4b2c0327469bf5bfc9d730a192d4b98
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58930505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd6ff86b8818148fa6404b9f093c14a262ce0120cb34c363433f8cc67e76c5e7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:30:24 GMT
ADD file:1a901dbb7bbbc19bfb20b5d51710de51673890f42514cc08510611c3e1ded6ef in / 
# Wed, 31 Jan 2024 22:30:28 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 22:30:34 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:dccb1f222734589d9e070aaddaa42d045af1f9c15cc212687cb77b060d229c76`  
		Last Modified: Wed, 31 Jan 2024 22:35:40 GMT  
		Size: 58.9 MB (58930279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df37015c67cf5af783d72c8848265891d53282c01fc2a7a7c5ed8f927b89e993`  
		Last Modified: Wed, 31 Jan 2024 22:35:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:e8439d904478c12c75c19dffd34c19f74b46f5d6b0041b32d97d405963cd6f33
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53294918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2f14af35f00ecf3bc48a6ab76f1dcfb5d2f3f42a68701eb43ae7c8d155dabb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:04:09 GMT
ADD file:87abfb42fef6e59081707e46f69ab15badd568f3b9a80f6a3cacf0b8da8d1e24 in / 
# Wed, 31 Jan 2024 23:04:12 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:05:27 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:02c8bb16500b05b417ea779ce90ebc06ea427675a6ffbaed8ccc20f3b10f9de9`  
		Last Modified: Wed, 31 Jan 2024 23:29:54 GMT  
		Size: 53.3 MB (53294695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8bb7629377f1828ef798a7693cb55f1bd6b635d2d14611b487a2e646a4fb48`  
		Last Modified: Wed, 31 Jan 2024 23:30:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
