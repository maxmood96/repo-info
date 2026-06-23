## `registry:latest`

```console
$ docker pull registry@sha256:5620083c96ffb6f6296bbda84b2da7e822ed95d8df10de6434cee19c39fe0e9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `registry:latest` - linux; amd64

```console
$ docker pull registry@sha256:7518da9b12dd746278282a729dee2e65eabdeb449db4d0b28d46ef6e90308f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20121269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc3f1a4432290d5ac3341603f15bf99c5b2feb4a9e3195e530aadc66fbcc65e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:52:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Jun 2026 19:52:54 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 22 Jun 2026 19:52:54 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 22 Jun 2026 19:52:54 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 22 Jun 2026 19:52:54 GMT
VOLUME [/var/lib/registry]
# Mon, 22 Jun 2026 19:52:54 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 22 Jun 2026 19:52:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:52:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 19:52:54 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47465c9fe4b1438b5f9aed1cf7182de26087f6eda66eb23dce944b763673bbed`  
		Last Modified: Mon, 22 Jun 2026 19:53:01 GMT  
		Size: 245.1 KB (245051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269b60c1a347a7b2501df94ec2391af4c325bb9ef5a0cf5a4e6dd2e87198eb21`  
		Last Modified: Mon, 22 Jun 2026 19:53:02 GMT  
		Size: 16.0 MB (16031187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90c3e90567750f85e63c5ba884e9ef81f4839ab404a8f3dfd306e661018c6a0`  
		Last Modified: Mon, 22 Jun 2026 19:53:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4e1177a675ecd1759cde12c405d158ff166a809659e4006966a2b1a7c87123`  
		Last Modified: Mon, 22 Jun 2026 19:53:01 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:e648072cc326a080beaf294364129774fcc687e027bdff1b39d8fbf9161f57a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 KB (264549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85447bee306edaae59b1a341e1dbc8bf4732a2c09510b8ec46953ed4149418a5`

```dockerfile
```

-	Layers:
	-	`sha256:3f6a72b62a6e961cbb241afcc4d6a96d20be9f435b8846888d483eb85dab6459`  
		Last Modified: Mon, 22 Jun 2026 19:53:01 GMT  
		Size: 250.2 KB (250224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb37447a81d229f9ac51bff5d3a2ecef9875370c32a92cfc1050178dcbcc79d2`  
		Last Modified: Mon, 22 Jun 2026 19:53:01 GMT  
		Size: 14.3 KB (14325 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm variant v6

```console
$ docker pull registry@sha256:debf1bbb82f8363c05d718b47d8462f25464ead5ba7f14aaf807cd46eb080a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18710764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f523e342e6165f714262dae19a45889258f03e3971f8561b0860b1a0451f37e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:53:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Jun 2026 19:53:55 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 22 Jun 2026 19:53:55 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 22 Jun 2026 19:53:55 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 22 Jun 2026 19:53:55 GMT
VOLUME [/var/lib/registry]
# Mon, 22 Jun 2026 19:53:55 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 22 Jun 2026 19:53:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:53:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 19:53:55 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49675e901bc7ee3279849465dd21c1d3f0a085ba424de1ad6c29bbfe825b1b4`  
		Last Modified: Mon, 22 Jun 2026 19:54:00 GMT  
		Size: 246.2 KB (246150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0796372a36b485eb4ad5c10951d4e957c02cf6202c04b14bd880e3cd288ad444`  
		Last Modified: Mon, 22 Jun 2026 19:54:01 GMT  
		Size: 14.9 MB (14911409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c335e79da671d9cca0b062dbb52229249c59d4819f607d93f884a189db6e4937`  
		Last Modified: Mon, 22 Jun 2026 19:54:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bc80c596a11df65548e52807e84ea1830c88b097b450da52edc569e387b149`  
		Last Modified: Mon, 22 Jun 2026 19:54:00 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:c15da66c001848219db50da3a9e733e7fcf935866a57e1165187e014bd2181c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03afc45aadc8e252ffa13c0fbebc401d3ada8a22f7fe77219d81137fa0f04d72`

```dockerfile
```

-	Layers:
	-	`sha256:694fa6b99c0d685f53c3b345836766c9147e3c65c33de89e0374109b7676d0c3`  
		Last Modified: Mon, 22 Jun 2026 19:54:00 GMT  
		Size: 14.2 KB (14203 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm variant v7

```console
$ docker pull registry@sha256:616a1f6dfdb5f5bef8728c445fb6a8b3b3c28bd2df1e93e221a53b9ffee5316b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18399847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb1e2e7ca60f4f87d480370c2cd462a3e6b6c3ce34bf73af4f8d7fc600a25c0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:18 GMT
ADD alpine-minirootfs-3.23.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:18 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:07:11 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Jun 2026 20:07:13 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 22 Jun 2026 20:07:13 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 22 Jun 2026 20:07:13 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 22 Jun 2026 20:07:13 GMT
VOLUME [/var/lib/registry]
# Mon, 22 Jun 2026 20:07:13 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 22 Jun 2026 20:07:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jun 2026 20:07:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 20:07:13 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:177f8e1e6f831989320cf2b59b7eabd21cbf36804c79506912f3a81caff426f2`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba276f0074fe0348648a3903d9df307ec902f79b15981450b09d494e300c9e1`  
		Last Modified: Mon, 22 Jun 2026 20:07:21 GMT  
		Size: 245.1 KB (245132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff37c0068408b96c4fe7330fcd3567f6519bec08200b0db7700ae3739f7557f`  
		Last Modified: Mon, 22 Jun 2026 20:07:21 GMT  
		Size: 14.9 MB (14892250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67984739837d8ff6557c495832209d1ed9552af5bd638eed32243de8c285dc87`  
		Last Modified: Mon, 22 Jun 2026 20:07:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb2c962a45d2062a0b0ea3634b70ccd34511e8336fd68f0f85f45db038e48e5`  
		Last Modified: Mon, 22 Jun 2026 20:07:21 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:b857a399f02f36fff17a4d7f639b0b335a8886ea28bdb95f31a972ab9da4b9f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.3 KB (263264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa343a2dcd634f5d966470d8bd98865b77daef59469843c7260d53d6817e31b6`

```dockerfile
```

-	Layers:
	-	`sha256:d0f9181bbc03f36c592cc29dee30764936424b7b95390750b2b2a4ee6ed5bd43`  
		Last Modified: Mon, 22 Jun 2026 20:07:21 GMT  
		Size: 248.8 KB (248846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70bfa0d277a28039dd2f4481a44d6a1b32e92cf32b24479f36fe16d4091bdca0`  
		Last Modified: Mon, 22 Jun 2026 20:07:21 GMT  
		Size: 14.4 KB (14418 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:bc68ba48dae0e0423bb885c8d07d20c3210febbe996d38d54d32c574fda690ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18823580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d26a873d9c1c357f6f3be92297c4a68bbd39ab9d5ab84f47e57536e6085fbfbb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:54:06 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Jun 2026 19:54:07 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 22 Jun 2026 19:54:07 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 22 Jun 2026 19:54:07 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 22 Jun 2026 19:54:07 GMT
VOLUME [/var/lib/registry]
# Mon, 22 Jun 2026 19:54:07 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 22 Jun 2026 19:54:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jun 2026 19:54:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 19:54:07 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b7518a8a2c3c1bed624e92a35486bb1e8285483cbf07acacca0055e663b88a`  
		Last Modified: Mon, 22 Jun 2026 19:54:17 GMT  
		Size: 247.5 KB (247486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa447a3f3472696dd72ce5d846c0a3320427a4b66a4d145c0f75b3b6b9efb8a`  
		Last Modified: Mon, 22 Jun 2026 19:54:23 GMT  
		Size: 14.4 MB (14393623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9820381a21377d6acd037d614614166730498838c3c7ae002ed45187f57f41b`  
		Last Modified: Mon, 22 Jun 2026 19:54:17 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a64b0fc2c8b91f063efa410bddd7f87c333f50483558199043f4cf937c2701`  
		Last Modified: Mon, 22 Jun 2026 19:54:17 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:4d9c7d9a1006b9f738b7ed199743f52407d3e121adb8f2fb997b78f8574f53a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.1 KB (264074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3486d04d966812ecaed9a622bcb8aa4132f2f4bfa2fde48fc5baa5fa44d770e4`

```dockerfile
```

-	Layers:
	-	`sha256:a23244a655cfeb3f910678026112ded551569bac9fc20e3bdbab86d088027376`  
		Last Modified: Mon, 22 Jun 2026 19:54:17 GMT  
		Size: 249.6 KB (249630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61dd17052d3c74d8352064d26454acf889197fdc7ed0ca04e3f4530594f15a5f`  
		Last Modified: Mon, 22 Jun 2026 19:54:18 GMT  
		Size: 14.4 KB (14444 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; ppc64le

```console
$ docker pull registry@sha256:8743d907b6cdb2dd87f4ed94f822fd154b89063c523a09c242b909ff017f910b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 MB (18375981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f76541ae81a4b1d1ccca4ebc0385717d7c4bacfcb2c034053169d1e34a54eb6f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:49:25 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Jun 2026 20:49:27 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 22 Jun 2026 20:49:27 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 22 Jun 2026 20:49:27 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 22 Jun 2026 20:49:27 GMT
VOLUME [/var/lib/registry]
# Mon, 22 Jun 2026 20:49:27 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 22 Jun 2026 20:49:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jun 2026 20:49:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 20:49:27 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2afe4ddf70535a87895dd2928115f13eed6bd80bb630863f6b224ede37a652`  
		Last Modified: Mon, 22 Jun 2026 20:49:43 GMT  
		Size: 247.9 KB (247906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6560a44fce175ef47acf06550554be08c32cfcf71234304c92a0c75addf0b78`  
		Last Modified: Mon, 22 Jun 2026 20:49:43 GMT  
		Size: 14.3 MB (14315166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd5fdef66691aba6224a0396b74054fe2dafc926047862087ba3588eabbddd1`  
		Last Modified: Mon, 22 Jun 2026 20:49:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c56ebedf1ae387efff134db775c1b0b4ee1620769345e48f68a80ef0273f50`  
		Last Modified: Mon, 22 Jun 2026 20:49:43 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:75f230ee32b15a03df499965af1a343bb46c2a63cb1b39ad27f9e3b028fde7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.0 KB (263978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71897556fbe1f7c56e5b37daceb2deeb74fd011fb04fee6437999dcb5900a23f`

```dockerfile
```

-	Layers:
	-	`sha256:6fc344e4c8c00da110031c1eda4bb79b2d63ff8a9f4d5256e4bac361759204d0`  
		Last Modified: Mon, 22 Jun 2026 20:49:43 GMT  
		Size: 249.6 KB (249607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:789ecb938ce7bb106c3aa07f346d8a17b45b611ec278ac19b4961d1c3d3e1141`  
		Last Modified: Mon, 22 Jun 2026 20:49:43 GMT  
		Size: 14.4 KB (14371 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; riscv64

```console
$ docker pull registry@sha256:6bac5ab784ef1271ea9c19fe949e249e46781a8de8e74f5d5eee4d2333d83e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19195319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1d893b9dfa1fceed9ded71ee8776f67539424e006b0c95b79818cb4e148f8f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 16:18:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 04 May 2026 19:09:59 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 04 May 2026 19:09:59 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 04 May 2026 19:10:00 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 04 May 2026 19:10:00 GMT
VOLUME [/var/lib/registry]
# Mon, 04 May 2026 19:10:00 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 04 May 2026 19:10:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 19:10:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 19:10:00 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3257359d78e33ee12c186b4248dac6627cb8e26d6fd747ad8f46ed2b4fb8e1`  
		Last Modified: Thu, 16 Apr 2026 16:19:53 GMT  
		Size: 290.6 KB (290553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7229a593c1ad909b80cb6562febfcb3c3ae614360f60e39f3df6b630c4b88f`  
		Last Modified: Mon, 04 May 2026 19:11:00 GMT  
		Size: 15.3 MB (15316494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd35c839b775367c12cccd08b74875815de87b7f413f1cf27d6c57422475602`  
		Last Modified: Mon, 04 May 2026 19:10:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f258677fb76704bf74854662f896fa858e0f752eb366cb4db17e726d5a2547d`  
		Last Modified: Mon, 04 May 2026 19:10:10 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:733beffa3194e41d1ee399b26ad63dc14aa216b30a95b9717c8d08a45017a4a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.9 KB (280866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755f0a1e30786f79a24c7473ae1e05cf0721d345db3b4eda3060c12905b1c824`

```dockerfile
```

-	Layers:
	-	`sha256:96f06bc2cdfa4dcdd98ff60faffcf5f6e32bcd776b2bf063527786625546bbfe`  
		Last Modified: Mon, 04 May 2026 19:10:57 GMT  
		Size: 266.5 KB (266495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57212effb84c519d6d4d843f6bb8a8d3475a11839fe208599208326c2d7541a4`  
		Last Modified: Mon, 04 May 2026 19:10:57 GMT  
		Size: 14.4 KB (14371 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; s390x

```console
$ docker pull registry@sha256:3258c57f1d3f616a9c806f1a5784a24343b7f87725f8f6ad91dd551069236aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19315005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd2f7875d22841f8cac8e57cc35361b9e7d3a6edb1db15bd25a30e892c501e1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:10:55 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Jun 2026 20:10:56 GMT
RUN set -eux; 	version='3.1.1'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='6f330a3ba9ea1d23a6ee189f449d792595240585bb2f159123d76ac594f70dd8' ;; 		aarch64) arch='arm64';   sha256='8167316d2b4a57e10d44f8c8a3c75fea5f3ec1c71872760bb903e5e8e52e9ad6' ;; 		armhf)   arch='armv6';   sha256='8cf93e43dfddb195f46dcf3e643d021f29c689a2662d1edb1e70f536f380e3ba' ;; 		armv7)   arch='armv7';   sha256='23bfb562d2b41dc6cb800fc7a2ea682071999ebb4c6e7c8162988bc49eb10ec3' ;; 		ppc64le) arch='ppc64le'; sha256='7f7e126b18b3deb1eecf14824bd80215cda6a10bb07a47c7c42268319cf5b305' ;; 		s390x)   arch='s390x';   sha256='27f5f3237a6332b129d7383066eee99f15759f9add9304fbf283cef1e3803041' ;; 		riscv64) arch='riscv64'; sha256='a64bb17c994885382c977d73695a3f000e884c25b8e5aa14857fedaa096619bb' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 22 Jun 2026 20:10:56 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Mon, 22 Jun 2026 20:10:56 GMT
ENV OTEL_TRACES_EXPORTER=none
# Mon, 22 Jun 2026 20:10:56 GMT
VOLUME [/var/lib/registry]
# Mon, 22 Jun 2026 20:10:56 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 22 Jun 2026 20:10:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jun 2026 20:10:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 20:10:56 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470176434bca20b0199baf086b0e5f5cba5a0bee165b8e1094c1885f4df27c81`  
		Last Modified: Mon, 22 Jun 2026 20:11:11 GMT  
		Size: 246.1 KB (246139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545862897924bceb9b97706f1c73c502840d540e039fbbfa46185c45a6974d23`  
		Last Modified: Mon, 22 Jun 2026 20:11:12 GMT  
		Size: 15.4 MB (15361009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6621ef0e5bc723e6e9b9c7415f73b4722e858f3f3da35efa99743b9f3831adaa`  
		Last Modified: Mon, 22 Jun 2026 20:11:11 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b26589d17656b50ffc9938cfc210eee544658f1fea6099fcf7f77eb16b247d`  
		Last Modified: Mon, 22 Jun 2026 20:11:11 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:ff9fcd6da3aa8ae0465188650111b05121da6e14746a25bb053eccb91ca8bf19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 KB (263898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dfc6aa19a21eb4a4b8376bcf670f0e355ca90a8fde035b19a2561a8f29c42cf`

```dockerfile
```

-	Layers:
	-	`sha256:9909b60e831886a87b34f8d8e20ec9466084574861f51acff91b12b80b9bc5b1`  
		Last Modified: Mon, 22 Jun 2026 20:11:11 GMT  
		Size: 249.6 KB (249573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02e91698fc78c29df6054e23b67d3e797a740990a861d1b805027443af1d2438`  
		Last Modified: Mon, 22 Jun 2026 20:11:11 GMT  
		Size: 14.3 KB (14325 bytes)  
		MIME: application/vnd.in-toto+json
