## `nats:2-scratch`

```console
$ docker pull nats@sha256:f4cb1bbb7e672124a6564eaf7026bf997f1659404f89b8c2e9bfc1883d7c49c6
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

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:d6cb6ec885a324dca2b830829bf9d4c5e43d41279805ce67be044db0ec7fae56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6598587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5ec0ef7d756ea786e6deee1fb08986ad9ab7616b087e445e2b3c73bf7f2d347`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 27 Jan 2026 21:10:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Jan 2026 21:10:07 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 27 Jan 2026 21:10:07 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 27 Jan 2026 21:10:07 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 27 Jan 2026 21:10:07 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Jan 2026 21:10:07 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:2f8912005071f27ea416bffea2294316df3b1b12b1e8346b2a1adcd792aa8496`  
		Last Modified: Tue, 27 Jan 2026 16:11:14 GMT  
		Size: 6.6 MB (6598078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05852294398b9aea33a8d9d248d324ee895e96dee6bfa8363653f16079ddac04`  
		Last Modified: Tue, 27 Jan 2026 21:10:11 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:a0f34e28b55652588fe8c7891ab83879808bee3cee9dbea0da32a6d4431fcc89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2ed37d6666a700ae3e29116b15949d1ff6130503d9cf7d5eb2620f33e201a5`

```dockerfile
```

-	Layers:
	-	`sha256:4e22704ce89be3ca5373eedf4cd92a430da69b69b5c4722a9b652a13f5009e01`  
		Last Modified: Tue, 27 Jan 2026 21:10:11 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:f7799b4a822c5771e5d48f0f1c068ea2cec23162c6831f82d2b009b36a857e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6323105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370df6c853d90e83658a3dfb4c82a802848ff4f6b4522ba921e6a7ad306ef356`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 27 Jan 2026 21:09:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Jan 2026 21:09:46 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 27 Jan 2026 21:09:46 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 27 Jan 2026 21:09:46 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 27 Jan 2026 21:09:46 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Jan 2026 21:09:46 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1efb0795d882364e2a023f0af5959b157fb2940eacdb92639318b205267c0ad4`  
		Last Modified: Tue, 27 Jan 2026 16:11:11 GMT  
		Size: 6.3 MB (6322595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a063463df74c77b9460e1541bdaf2c37a26d18bbe62f9c9260bd94e67282330e`  
		Last Modified: Tue, 27 Jan 2026 21:09:49 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:d73a9779831083ed543a3bd2f7e87c1dc8caec08ddac320cc7a25c94e648b157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6301a8cfa90733ef8a35c4bde2ee64d946519b1026091f17c5e915f86a498204`

```dockerfile
```

-	Layers:
	-	`sha256:2e565ea89cf46f2c719698d7f99d288200307fbb51c38e98a8bde6c8102d0d23`  
		Last Modified: Tue, 27 Jan 2026 21:09:50 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:488c6c4014617fff07b617db250920bcb069b5d712e4185c98c6387b2baa93e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6310862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b7a85a207a36665f5bc23045e4bba37e6a52dd82b9b57a47b543b28fe145b20`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 27 Jan 2026 21:09:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Jan 2026 21:09:09 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 27 Jan 2026 21:09:09 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 27 Jan 2026 21:09:09 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 27 Jan 2026 21:09:09 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Jan 2026 21:09:09 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:f89bd8d5669bd18e009b01f3649659381ff93c4199e64ffa25637a2739cba3a5`  
		Last Modified: Tue, 27 Jan 2026 16:11:12 GMT  
		Size: 6.3 MB (6310353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c736e7cdb0b623e13835c5b7f1ff18a1b684a47db62f5986b4a18586e605dd0`  
		Last Modified: Tue, 27 Jan 2026 21:09:13 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:9fd3d1e91e30c408f98d4afaaaa4bc75c40efeb43567518934829f6d0ac86556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f796abff51fa066462285403989439d8035c748d22d1b340334a21cc658983`

```dockerfile
```

-	Layers:
	-	`sha256:13865f9df2b0d2a106a6ff2b46ab7f923c9d9bcd479a551759a737f5ebcd44a1`  
		Last Modified: Tue, 27 Jan 2026 21:09:13 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:ee00181a83f1e714e9c4c4d6e35b6bd124ad436002ff006416bf5d0449730609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6009835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78df69576498e4e17dbf23d118023446e537e850289aa5393328b06459bdc44d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 27 Jan 2026 22:10:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Jan 2026 22:10:23 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 27 Jan 2026 22:10:23 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 27 Jan 2026 22:10:23 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 27 Jan 2026 22:10:23 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Jan 2026 22:10:23 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:e69d87f2a1b2cfbc091bf2d3af13a1d9188b163cbfbce527d6fb245cd470e987`  
		Last Modified: Tue, 27 Jan 2026 16:11:12 GMT  
		Size: 6.0 MB (6009325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89399e8d1cf32196628af8c6ad59289948735929b8b1b38523dfa1acf32630ff`  
		Last Modified: Tue, 27 Jan 2026 22:10:27 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:a5dd95deed7335935075ca0769fc93c1bdb114d90e5b3aa4852ef42812b646f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:183a24a65922d46207f3a6d71328cdecf7428afe789ec090ac0ba934b510007f`

```dockerfile
```

-	Layers:
	-	`sha256:629797c20b5f620ab2384df0ebaee6035c43024dba879134a4767d3cd71f1467`  
		Last Modified: Tue, 27 Jan 2026 22:10:27 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:98765b2b71bf6daa662b7dbd1055075a97e9000f3758c6aceeb26c8cb5fd0e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6059945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f209e000ef99dbbbc6d350eb39ac8c75f5d40744f18ae5414c0c07e9e45655`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 27 Jan 2026 21:09:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Jan 2026 21:09:35 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 27 Jan 2026 21:09:36 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 27 Jan 2026 21:09:36 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 27 Jan 2026 21:09:36 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Jan 2026 21:09:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:d7498e46ed99a6f25a5e161fffb2a10e547d3bd8f682806db51e70bf75c104d8`  
		Last Modified: Tue, 27 Jan 2026 16:11:14 GMT  
		Size: 6.1 MB (6059437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acc876a389815f30f4ed7cc57a5e9f5567f01329f4b7342b268c005c27834a3`  
		Last Modified: Tue, 27 Jan 2026 21:09:46 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:43af96803f49adc8aaa465d03d0dde41ee7e209f9a0e28947566a936727c49fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3421e3e523f67cbeb606c276691497e77d59a9afe368fac3dd2b77b44a4ceb58`

```dockerfile
```

-	Layers:
	-	`sha256:e3c3d1d8ec6a07a1fc217e6f7df3eab02aa21e7017b3693f928a7360d8ac21a3`  
		Last Modified: Tue, 27 Jan 2026 21:09:46 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:ae3f7eac492fb3850591ee0580f6f26c3ab90fa4001072f347bbdea377021180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6439573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4204c3fe6f38e529b9ab99128f4f71c742b5dddbec6d3fcdd784912c812e359d`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 27 Jan 2026 21:09:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 27 Jan 2026 21:09:36 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 27 Jan 2026 21:09:36 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 27 Jan 2026 21:09:36 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 27 Jan 2026 21:09:36 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 27 Jan 2026 21:09:36 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:647f636b2ba788fbcd64742e49cd42dbe55579be711374f52ac5c9e3bb6810d2`  
		Last Modified: Tue, 27 Jan 2026 16:11:14 GMT  
		Size: 6.4 MB (6439063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930f40f7174a2c941bc3d6fea3291abdd5910b116dc8976147ffe92096a2dc89`  
		Last Modified: Tue, 27 Jan 2026 21:09:43 GMT  
		Size: 510.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:363dcabc130a83ffdf947725601f3ff72e57b4ac101c352b9ca592bd1e8678da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81e58884f9d9e0d8eb1b6185d44e98751a7fab46989c675f9307e30d5310c55`

```dockerfile
```

-	Layers:
	-	`sha256:c10d7d82f5e8df9bd31c438ff05420d632a2ad10dcad8309a3de4d55d2196ce2`  
		Last Modified: Tue, 27 Jan 2026 21:09:43 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json
