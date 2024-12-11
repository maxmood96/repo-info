## `nats:linux`

```console
$ docker pull nats@sha256:88e88d83db1f6e1313f379bea842fff60f9914f9ce71e50b1dfcf89c7f914a39
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

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:6bd4f64d1352a927bccb2ec6b2fe1cf728f18c25739c3b78d78464b71a5c3407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8517583dc2cbc6370e15061a372ece9ab0fc67f3482f727e34d262259b444e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:725abe751c1168aae43bd1e92a8d8556040c49873798d5c7db308ee3cd5c7089`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 5.9 MB (5904958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e4dcbbddf2a8a406b42bacf100e91cfa466f2a5a5a57bf65978c52820ee75b`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:f6894f261b71ad16501257715a52f7a6d20668e60fe924540192fe904b446303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d2a6b34adcd30c1e5b08a14589d1db94793ee54a86619681827e798d1e8286`

```dockerfile
```

-	Layers:
	-	`sha256:a76696a0f138faf1089233faefcdd2a02a2d52ecd4af375249edff7201085abf`  
		Last Modified: Wed, 11 Dec 2024 00:27:37 GMT  
		Size: 10.5 KB (10473 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:e2c73f664e5f7e8fe1c54de04ef12ca65e5999a02613b3494911b46f487e5c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5555743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf8576cc8951bfbb3acc6b45dd34f6376dda13c2f9498e57ba857577c99630a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:3f85eba4fa44ada167d34b4fd66d1e9ba19d5f77065ed1a2f444057c3269d999`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 5.6 MB (5555233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369165ff8bad27a89ae21931399ace0381e3d7aafdf8fbbc63ff96082fea9222`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:17112a8bb3d19d806862c7dcce437d4c34c16aaf7a0a541cbe88ae7dc31ebe44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c76ecbf3f249ef6934f5a7aa4cfe4ccc3fe022d7fd015ef43122812595f4a7`

```dockerfile
```

-	Layers:
	-	`sha256:7304562cf2a56789d58682dfc1364b6901f9602a05a5962e90a768584cd9d9cc`  
		Last Modified: Wed, 11 Dec 2024 00:27:35 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:db51490617700db459fb28b393275f487143e2b213dda576fd209b359c17de7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5542345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6209fd70f508eef958e9a0610a1e1cb27aee0e27a9c07a9dc77dbd390f7e7c4`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:4cf6f190658e498a5ede44fcce29d6e47c92dfeae417a299c917e91770459446`  
		Last Modified: Wed, 11 Dec 2024 00:28:07 GMT  
		Size: 5.5 MB (5541836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9647c38859063c5747990e2127f1a9b7cabb93f2acf7623986e146e468633281`  
		Last Modified: Wed, 11 Dec 2024 00:28:06 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:ac4ae941c9dab3a62fad62fd2cc28f7e5ab25c82f9d9c46672e07b931be89f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c0da7f65b97baa443f08347ddc9c4d3ec842a55c3613808d59666669648b80`

```dockerfile
```

-	Layers:
	-	`sha256:f46e0d405121b055cc447b67d83479b8c33462f3eb1b90e0b8150f78d3a0cdf8`  
		Last Modified: Wed, 11 Dec 2024 00:28:06 GMT  
		Size: 10.6 KB (10600 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:4a4e64a0aa6c6c28902ad531e751ca186ea840c4bdf4921450f6d7f90e9a06e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5453533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a09d40f9ef634b3e1a7ebeef3debfedcee9d447a300893633606acd201c3bfc`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:54436bf7673c09249d2515eacff74e8a7d6273bd4d16f1ad1414e20c12eeeb26`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 5.5 MB (5453023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14eca72e9ccaa25f137f8b7fc9c5c7352f342c9541006fe1f3fdf9681200468b`  
		Last Modified: Wed, 11 Dec 2024 00:28:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:d434741e87ef7fd586d68e3a22f6576cfe0c35cd318d342f644dbb981ac24115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 KB (10658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3ee70e7d7400565a96db228b06c55b37cc929fa6b22afe699332ccada2757f`

```dockerfile
```

-	Layers:
	-	`sha256:fa73bbfe1b34c0bf8c905bb2e1be1a4693f74011abff00b1bf3a8abcc56bf9ec`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; ppc64le

```console
$ docker pull nats@sha256:80e254782e4673818b62d9dc06dbeaa0a72340f5d3b047add70925d0d00ac24d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5419246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4796bbc2b1693bbd908b212184cc9be10d1c168480cb0050afa939cc95ad29`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f9f6592a006b5b5f3c6032c79b9d35ba12543dd547bdd5d7a363f4ab86ccdf1d`  
		Last Modified: Wed, 11 Dec 2024 00:28:15 GMT  
		Size: 5.4 MB (5418738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d9f4c7c296ea544ec5b8fa13b1e42d5b5737a47962eb328e9f709512f3d993`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:bdf13776c5d49a3c0bdfe12a5164e64bd1afc2290adc241f6b0c7072730a3e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f26a731b8fb385c2f443f693e95ad01bb7d65fc7033ac6ad2550ef93301eb0a`

```dockerfile
```

-	Layers:
	-	`sha256:bfe7de1f670e415231fc72274258b4b628daa0493cc537a45fdb1e35591c57bd`  
		Last Modified: Wed, 11 Dec 2024 00:28:14 GMT  
		Size: 10.6 KB (10563 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:linux` - linux; s390x

```console
$ docker pull nats@sha256:da0242ead556d0d9a382140a01876dd503595eb64b34e15c39e223312af1aea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5749128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6639a3d6b8ac1ca5effb561df3d7ab989acc4d44f63e4957568dbc0192b6624d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 10 Dec 2024 19:41:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 10 Dec 2024 19:41:25 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6931be03dafc088764c7dcb48f17bb6e112cbc980d50d35e26d43ac870238495`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 5.7 MB (5748618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227edda2ecaf071b40ebfba2d62a9426bec4019463aca86b9663489d6a77d90e`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:linux` - unknown; unknown

```console
$ docker pull nats@sha256:4becb503613be96c5cd4054a51c7cbfa4ee5b751616e0ad7ece6520b9f23a7ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6688c8a1fd71cae2abf7a1f16406f0d0e1487f6823506faec2697dacf9c0a57`

```dockerfile
```

-	Layers:
	-	`sha256:37690a2ab045115f8e2661c547ab9543cd72c1436055d243d50e8e75c182b863`  
		Last Modified: Wed, 11 Dec 2024 00:41:23 GMT  
		Size: 10.5 KB (10472 bytes)  
		MIME: application/vnd.in-toto+json
