## `nats:scratch`

```console
$ docker pull nats@sha256:82e8c34b1b203fcc3e8e563da83abf1fafc5286d086520b99c460b0b97338bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:cbf394e77b0b11f0d67241c1eb5dc4f38f1f831f7cc78ba0a99767e5f3c77602
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4555490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38955d8eb1db8dd876a018c7ffec6306039b28162a2a3f659f20ad765b4d7702`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 18:21:07 GMT
COPY file:41cf24bde0db51aec4d8f2f448181be039d405cfa2a029cc91c2610dd3a7215a in /nats-server 
# Wed, 22 Sep 2021 18:21:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 18:21:08 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:21:08 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 18:21:08 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c176eb757cf8fdb1af8fccce4e1186772bed0896689b06eeceaee0edb56ecd0`  
		Last Modified: Wed, 22 Sep 2021 18:22:02 GMT  
		Size: 4.6 MB (4555013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8cc7e3d24c61c54810d11e98bba6062d04b7689036a2a1ca1c516f09b033dae`  
		Last Modified: Wed, 22 Sep 2021 18:22:01 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:42b581db1978366653049e22ccb5b49c9052e32b5196b14a96937761f5963b1e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4218594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcacbf7ad430ac841ac0f170d987a8e9c6e07a25f2b2b85b811a97b467cab5b6`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 18:50:08 GMT
COPY file:2c0f511373a5dc3c929ee9d46ad4f6fd6ebfc976a5ad185333a651b90fd1f7db in /nats-server 
# Wed, 22 Sep 2021 18:50:09 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 18:50:09 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 18:50:10 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 18:50:10 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:02529d896ecfdeb48e7347579398a35f4c20e360e6d850e79b70358e1e2e961c`  
		Last Modified: Wed, 22 Sep 2021 18:52:33 GMT  
		Size: 4.2 MB (4218117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2463a1994b43cc34b85ad06b56cda40f17f7a711ec73e37e4a1633c38b9ac861`  
		Last Modified: Wed, 22 Sep 2021 18:52:30 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:aafbb0b5e1b7412f9d0e71ddd6c3948c7080697882dd40ae20578b855ca40c1f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4206272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f5a4fb5f9254997b2d7e573f24316740a167eb829bb23952ba05ff8304ddc1`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Fri, 10 Sep 2021 00:59:05 GMT
COPY file:7043dd814cd92048127f9905d58e9204d2968d9c03bbb7feba592c45a87e9963 in /nats-server 
# Fri, 10 Sep 2021 00:59:06 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Fri, 10 Sep 2021 00:59:06 GMT
EXPOSE 4222 6222 8222
# Fri, 10 Sep 2021 00:59:07 GMT
ENTRYPOINT ["/nats-server"]
# Fri, 10 Sep 2021 00:59:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8ae70a7ddee0b3bc3819ff86ee31d3295a37b10282b7ee0d14d3dd3c8dcb16c7`  
		Last Modified: Fri, 10 Sep 2021 01:01:28 GMT  
		Size: 4.2 MB (4205795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbbfbfa45875dc8bff20ba3a989407cf3ab8018f98f4277411dd068510c071c6`  
		Last Modified: Fri, 10 Sep 2021 01:01:25 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d2ef35e762b15ba3758768ab244dd517de38c2b415c2fe3e297e93948337b0ce
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4167854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c25200d88dae335f7edd708c0d0c41d5be7112bb77be4c91912dfb0a1767e1a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 22 Sep 2021 19:06:14 GMT
COPY file:73474745ed57d919ed2564494c691c14cba8ce4edf95bfb12936456d7c275828 in /nats-server 
# Wed, 22 Sep 2021 19:06:15 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /nats-server.conf 
# Wed, 22 Sep 2021 19:06:15 GMT
EXPOSE 4222 6222 8222
# Wed, 22 Sep 2021 19:06:15 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 22 Sep 2021 19:06:15 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:dd8bb97900411606b59cb3c37b8140330e2fdf22f61f7c61a8b5ce4bc01bce23`  
		Last Modified: Wed, 22 Sep 2021 19:07:40 GMT  
		Size: 4.2 MB (4167378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e276e3d19b7cbfd289bef18362b920d2173ac41b3efcd5b877bed6947cb65ea`  
		Last Modified: Wed, 22 Sep 2021 19:07:39 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
