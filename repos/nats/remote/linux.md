## `nats:linux`

```console
$ docker pull nats@sha256:a6e14c0a1cdf2cf257399bc543c04707b967ebc2cb8ec182ce1d6780e5942009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:4c4e804a1650e91fbfbf07efa44afc479755a6ace2ab57050b950475ddc93442
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4575849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acde872f934ff8c9ad3505d331c4827e3285ad4314e92f69ae0abe1d455ff77f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:42:18 GMT
COPY file:148643ead7a90f9c3416e4455a70bf4638bf9c77005e258d6ec4dcf605560028 in /nats-server 
# Fri, 19 Nov 2021 23:42:19 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:42:19 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:42:19 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:42:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:fe89a8c692b8dabfd4ac3062f9232c753d0c2db79be5dca06811cfd9dbcbdc1c`  
		Last Modified: Fri, 19 Nov 2021 23:43:09 GMT  
		Size: 4.6 MB (4575375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5645a0f80ddde9dcce3a4aecfc7a9ab65b20f5c4fcab9897e75302b2b4bf404`  
		Last Modified: Fri, 19 Nov 2021 23:43:08 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:54395301fd2f315191df081131cd6d142613d057970268d64480f4706bcaeda3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4241317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4851d5f7b19bc49c52879a43236bae3e26e03a8a0f035ec150eed9a723cca5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 02 Dec 2021 22:50:02 GMT
COPY file:6036f30fae4132d78e941219bf965a4e4c3e6d898ac912ab22e7a0cc98adf5a5 in /nats-server 
# Thu, 02 Dec 2021 22:50:03 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Thu, 02 Dec 2021 22:50:03 GMT
EXPOSE 4222 6222 8222
# Thu, 02 Dec 2021 22:50:04 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 02 Dec 2021 22:50:04 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:41ef8f0f5e4d1f0e1880325ac8c2ccde63d323e6ead77b97c1225e0ce1d226ce`  
		Last Modified: Thu, 02 Dec 2021 22:52:29 GMT  
		Size: 4.2 MB (4240841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e8f034153e28423592a04f327fe3b69d3d84721cb54631e3ea9dcae375ab0ef`  
		Last Modified: Thu, 02 Dec 2021 22:52:26 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:c3e6b4d51c17fa68c6e4c70ce519e1035c89a232b96c9ca59d1aa9932f7b4687
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514f8bdd0d1db9adfcc78eb1a00c34ad3eefd5e7135852bcd277023ebe30f0c8`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 19 Nov 2021 23:22:48 GMT
COPY file:48132b2177bf3ca4d978b99a66b7a228cae6937450ee016ac753a4c4ffb567a6 in /nats-server 
# Fri, 19 Nov 2021 23:22:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 19 Nov 2021 23:22:49 GMT
EXPOSE 4222 6222 8222
# Fri, 19 Nov 2021 23:22:49 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 19 Nov 2021 23:22:49 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:92ac13b7cd582c606500bbb3364dbf1a7e0a85030b4deeabfba3a44d94b2c66e`  
		Last Modified: Fri, 19 Nov 2021 23:25:11 GMT  
		Size: 4.2 MB (4235210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b8c68cfe1eeaa6a60a3863fceb15216ecc6b46b1ff00255bffe9a638b3b768`  
		Last Modified: Fri, 19 Nov 2021 23:25:08 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:8ecffb2097f683980b94450d536a99c79b3fe7654f8bc91fd1c45ad0825e6aae
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4189764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bb404fba49386fc48ceb05ee04604d317ff225da69f159d0bd4cc63a930c0e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 03 Dec 2021 16:57:31 GMT
COPY file:b5f62686ba6debf89a42d2be7c4442db5f8735dba6b8932e6f01f315a2e63e27 in /nats-server 
# Fri, 03 Dec 2021 16:57:32 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 03 Dec 2021 16:57:32 GMT
EXPOSE 4222 6222 8222
# Fri, 03 Dec 2021 16:57:33 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 03 Dec 2021 16:57:34 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:44ff62bde832e2b2bca85708fd2fc86d7d6d1f4ca7c58b5d0e18e3d07c9c5bac`  
		Last Modified: Fri, 03 Dec 2021 16:58:50 GMT  
		Size: 4.2 MB (4189288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44dcbc70566b6f8312605c0214812444ccad7a55594fa2e7f0792c21af818ef0`  
		Last Modified: Fri, 03 Dec 2021 16:58:49 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
