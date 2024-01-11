## `nats:2-linux`

```console
$ docker pull nats@sha256:d6c08cba2c17bb41fc380cbe2d6108b6def194abc281b1ebe219d6e37e85ff30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:cfc16611986dc5883f4d27c9085e76910343d967594ee383d0255baeb057db79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5501382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd357d7a18b1dda228ed5178c5ca385155fb364d30c57ca494ff97c8cd19309`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:39:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:48:54 GMT
COPY file:bfe22f1af895b2fc7a50837842688e659c05693b4bf069ba0376ffc69ae697ea in /nats-server 
# Thu, 11 Jan 2024 02:48:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:48:54 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:48:54 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:48:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:7acebaf66611006473295971042ce1d190371c2a188cd83ac1294bdcbe941861`  
		Last Modified: Thu, 11 Jan 2024 02:49:55 GMT  
		Size: 5.5 MB (5500874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eaf929d718cd812eb25392358200a35e1e26347e9cfdce5e0b620aa8b735742`  
		Last Modified: Thu, 11 Jan 2024 02:49:54 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:ab622a448169a02769669a9f3de1ce7e141dae7352f0521512bdd6c6038c3679
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5218996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4bb91325553db1e40aa41a1ccfc3269b9d976da5f9adedc209a24fe602fe4dc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:29:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 07:55:44 GMT
COPY file:14bb9d2fb0cc787a50e753f389a7cfc3a478e7bc39d63aac532a65510868583f in /nats-server 
# Thu, 11 Jan 2024 07:55:44 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 07:55:44 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 07:55:44 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 07:55:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3465331ddb86c2fdb86ae6c9eaf7b4d6b07cd12af9962e8b10f97adf2dcad6fa`  
		Last Modified: Thu, 11 Jan 2024 07:56:47 GMT  
		Size: 5.2 MB (5218488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc425bce7b52cdef9f280a1875c3e8f9cbc224124419a884a963d3dc863bcfaf`  
		Last Modified: Thu, 11 Jan 2024 07:56:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:a64d6b7675f0097a69544912df42b5d4e9b121bfff34649843637c53ab640cfb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b3ae88cd2cd670d8b9b7f6e610fd3eb8687d499c38ca124f8033d847bbe8881`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 00:53:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:55:20 GMT
COPY file:8b6480435610d9164cd2c66bf75ef01eb81c3073e740cad17c74339e5baedda5 in /nats-server 
# Thu, 11 Jan 2024 02:55:21 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:55:21 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:55:21 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:55:21 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:0920770a264f958a57c4e11d9c31cf4441041ea655047f6e857b67fad43906f9`  
		Last Modified: Thu, 11 Jan 2024 02:56:29 GMT  
		Size: 5.2 MB (5210357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c60b3bdf3047e4a3391384685743bd7f58305a89f5c71bd9b22fcd6e30211b`  
		Last Modified: Thu, 11 Jan 2024 02:56:28 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:187bdea269fa2454820b2e7d8e40ff4c70919e9caeac33af047e45e86f4e9118
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e480d5474031fbc4d95f443dc0e87b2d5bcfa6936887c9c20ddc78880966d3`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Sat, 21 Oct 2023 02:14:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 11 Jan 2024 02:49:59 GMT
COPY file:8879823466eafef24f1fda27c9cd4f809446ce0288c6939e09932ffe25ab7b19 in /nats-server 
# Thu, 11 Jan 2024 02:50:00 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Thu, 11 Jan 2024 02:50:00 GMT
EXPOSE 4222 6222 8222
# Thu, 11 Jan 2024 02:50:00 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 11 Jan 2024 02:50:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1e7857182cff537484895387bffc3495ec32bd159979fa4d1b851b83d7cd87c3`  
		Last Modified: Thu, 11 Jan 2024 02:50:57 GMT  
		Size: 5.1 MB (5075684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ac1735dae6ad6bb18f1075bbad502a9dc797d686f5c92486bd72aa9c38499e`  
		Last Modified: Thu, 11 Jan 2024 02:50:56 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
