## `oraclelinux:7-slim`

```console
$ docker pull oraclelinux@sha256:c0036230a9748c90587a31901b9bc51761a289d8b6a3de60d3b73a08d96e9510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `oraclelinux:7-slim` - linux; amd64

```console
$ docker pull oraclelinux@sha256:7af571e5ad0b582c88271769cd622514e83d90c65bcffdd5fd3ca3b3fbfa80bc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48257819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58346d09e3bf577a9777bd1b694117316ca9a44434d46630a8852f854c596542`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Sep 2020 21:23:41 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-amd64/7-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 7 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Thu, 17 Dec 2020 17:36:01 GMT
ADD file:86d6ee7b986b86b9aa79210fd979dc5e350e434afc9b6897d52373bf8e99a3b1 in / 
# Thu, 17 Dec 2020 17:36:01 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:aaf2c1f8a217b022b582b2fa29293a3e7bc90ade4849a2254c2a44eb2391396a`  
		Last Modified: Thu, 17 Dec 2020 17:37:11 GMT  
		Size: 48.3 MB (48257819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `oraclelinux:7-slim` - linux; arm64 variant v8

```console
$ docker pull oraclelinux@sha256:a6964517b2916b8f1b091f1a97edb63c792c5474a18a07963bb0b25c530da29c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48865698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b424120f0c3a29318d5e8e355efc9b45ce2d3d9b24d74adc983d9850bef6ffe4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Sep 2020 20:41:36 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-arm64v8/7-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 7 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Thu, 17 Dec 2020 10:54:39 GMT
ADD file:234e637b79d352a87884f78cc7eef7b15ada4bb4afd2ce527325eb690092902f in / 
# Thu, 17 Dec 2020 10:54:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0c52f25eeb980aa519afffa967e1c689524d7fde7d50fc33420a3d54daed23da`  
		Last Modified: Thu, 17 Dec 2020 10:55:54 GMT  
		Size: 48.9 MB (48865698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
