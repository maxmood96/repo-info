## `nats:2-linux`

```console
$ docker pull nats@sha256:6dc2203f6a841bd81e88f4c6848649c173b0b54a1a5a7e297194514f9db92b08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:bcb3725766caeaa9675d714f44d1e08dd821c02765ba761f7b30e457e03b67c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6335604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e3af0381ca723de85cabecbc827fe835cbb57d1a83ad5a6286fffa7c7668ba`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6c51dc8c95848aa41be2d35f779bca5455ccdf564538c5bf731cc882473c2179`  
		Last Modified: Tue, 01 Jul 2025 16:12:10 GMT  
		Size: 6.3 MB (6335095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3c38ba4a87aa2fc0cf3d72b257ff8df016c65fef26ba1d30dcb8572667192d`  
		Last Modified: Tue, 01 Jul 2025 21:41:25 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:b6e99bf544161f7c9e529f8e2e94d2535adf9cf9dd8ce6d5b9093632d6388786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d77f965918b6239585603a4c4eec5ff5cd47e0c9960c53efafaa13ae592667c0`

```dockerfile
```

-	Layers:
	-	`sha256:a79888241c35acdaaea4017df54d0eb08cf99a033458ea969487e52e8aa83cce`  
		Last Modified: Tue, 01 Jul 2025 23:56:24 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:6f302a9a03915d7f6d6220347531d288e78144bbec898fc13d9bd64ad5f264f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6047667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ac6cab7f3eeedf218ac6cef0b2fa34afd373eaf6cdfb88108b9eb74f7f2e1b`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:ae84ac332de9f2d1f19db520980173d7a0d1212e5434b8131fab4bbb3f3430b8`  
		Last Modified: Tue, 01 Jul 2025 16:12:10 GMT  
		Size: 6.0 MB (6047158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f285b41634d621ace291c2fcaa9b61627b4982ed281e34feb36b3ec7b12a519d`  
		Last Modified: Tue, 01 Jul 2025 21:21:17 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:cb4c95e59d89fcf607926245864b5fa8a3fe252ba49f790c7b7716940854507d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9296bfe9eb7ba679a20140ebcb8fb6a4bdccf83942e6d2a361babf1202bd181`

```dockerfile
```

-	Layers:
	-	`sha256:9a708c8bff74339211852e0de0477d11a9153cf7cf1e0708a8a3afa2fb985874`  
		Last Modified: Tue, 01 Jul 2025 23:56:28 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:6a51f2cbe4249e5c34ca8cec89b19498adb28c5e0f219984cb8093a5ef3bc477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6037920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38f49a5d765f371391239a85151a2f3229a73c147291380dcd9d7409faf2bbd`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:5421471907aa6121cbe1e45fbfff9666eff9c457d77681eb748abf482c1f1863`  
		Last Modified: Tue, 01 Jul 2025 16:12:10 GMT  
		Size: 6.0 MB (6037412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0053e8d6abf738c77d5e3f2dc5d7aebd55a457cf3a067f0f3256c3bae11511c1`  
		Last Modified: Tue, 01 Jul 2025 22:39:38 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:9548176187103721ab070b8574227db7cadbe212e2e274be5814e55d3c69770d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594788c623bda7e1ad8bab421092850d434970284ac3388c131a72ab0f4ba241`

```dockerfile
```

-	Layers:
	-	`sha256:9ed84ed78e5a8705c9d5e1671ecaa1126886278c341e0d2525e2c15fe8c02e51`  
		Last Modified: Tue, 01 Jul 2025 23:56:31 GMT  
		Size: 10.6 KB (10593 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:429cf2ae1d174b89aaba6967efea2ad4937d13fff377897c6157642f98eab8ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5818405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec37d9ae7d0a6d32aa44b7114474f91a196a7ca505b4377cf4d17b5d15d95030`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6f47403dcac619d9e8a87b4ea67375f6b36474a5ccaefc9a9f741d63c73904de`  
		Last Modified: Thu, 26 Jun 2025 18:56:56 GMT  
		Size: 5.8 MB (5817897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b232165910bcddbb4814ee667f1c47f884c5dc640ed787fb49279714093311c3`  
		Last Modified: Thu, 26 Jun 2025 21:52:15 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:a5f1a6d09677f180d8310c2f3b6f1f50dfe44521cae9f6dfabd2d446e40e55d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6dd43a1308346e2d1c35bf60d2198d75b1fb95c69d1989d251df7c8cafc0be2`

```dockerfile
```

-	Layers:
	-	`sha256:87d6d83191487b0830bfe6b1b6b35c52cdaec6db66064ea7d9d64ca530ba12e4`  
		Last Modified: Thu, 26 Jun 2025 23:56:41 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; ppc64le

```console
$ docker pull nats@sha256:6d594bebb6faaa5f47d863601b3eaa1370539bcc24c4f23ef38d49bee3bb2c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5800513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbdf79a82a8d2f62140c8bc1db0e6c79d74580303ff6a4c65b6d0acb80c65cfc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 01 Jul 2025 16:09:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 01 Jul 2025 16:09:42 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 01 Jul 2025 16:09:42 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 01 Jul 2025 16:09:42 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 01 Jul 2025 16:09:42 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:555487709c5e1f1f15a63e67ac8d9ec8c857626166ade5c1dc3217a81051dcd2`  
		Last Modified: Tue, 01 Jul 2025 16:12:10 GMT  
		Size: 5.8 MB (5800004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3029869227b7ff12ef0c4c6e2f4e2831b3c4aa294a0cfe64b6904f64614f0738`  
		Last Modified: Tue, 01 Jul 2025 23:35:15 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:369cf895c049ede8833050f7e42a10d139c8d0200102af78f82862dc02d1a2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8eab4f64adc694e5d69df6c8fb1c8164583cfd04423a0319a1cc7fee42d621`

```dockerfile
```

-	Layers:
	-	`sha256:f3d874593d657eba9c8b4ab1389f4c55db094efaf7225c9c04ddcd5cb223a679`  
		Last Modified: Wed, 02 Jul 2025 02:56:26 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-linux` - linux; s390x

```console
$ docker pull nats@sha256:2f881eaf0c8e382bf708a0bbf181ee67a96b21c58bd02100f9edd2719825fb36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6164421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35a676d3d700bb35b0a293d157fc303b5a1944c42074cf75bf5815fdb04e86f`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 26 Jun 2025 18:55:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Thu, 26 Jun 2025 18:55:01 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Thu, 26 Jun 2025 18:55:01 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 26 Jun 2025 18:55:01 GMT
ENTRYPOINT ["/nats-server"]
# Thu, 26 Jun 2025 18:55:01 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:a1b7d98c93e3b3f954dd0d915cdafb90a61aaf4540a49f37ac9bdd94e888ed8c`  
		Last Modified: Thu, 26 Jun 2025 18:56:58 GMT  
		Size: 6.2 MB (6163911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c5b1389aef8f915ec9bf53345a388863995db7edc5a4b7fca0942a5a659828`  
		Last Modified: Thu, 26 Jun 2025 21:09:24 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-linux` - unknown; unknown

```console
$ docker pull nats@sha256:b806544044bb446452c20b800e6773579eac1ef36abe25ef7316063f69fa8119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f6815a5098733c736b0efd52b788f4a7ea17cad0c3008490fe1939ca50dac7`

```dockerfile
```

-	Layers:
	-	`sha256:dde9449017bba1801d9eb5009264fd7fb19a2678bac702c3a6d2d05b37fd0ee3`  
		Last Modified: Thu, 26 Jun 2025 23:56:48 GMT  
		Size: 10.5 KB (10465 bytes)  
		MIME: application/vnd.in-toto+json
