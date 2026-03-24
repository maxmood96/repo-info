## `nats:2-scratch`

```console
$ docker pull nats@sha256:81fb519cf3229a15af68b6c89342b09e89bbb0dc4dcafec9ced7a3c0137e8771
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
$ docker pull nats@sha256:f14e31c2594586efabf96d3978aa9b4c181ae095394c756b8ec2e773704c51ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6634407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb4fe3927ae68a52f09bfd3de902db0029ed53093017754dbb9b46a6161e1a2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:40 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:40 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:40 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:40 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:40 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:9c680bcbf3796ddccafe3aa9aa66d6f170e0ae39d7af37ad2b258d993dcc4270`  
		Last Modified: Tue, 24 Mar 2026 15:54:43 GMT  
		Size: 6.6 MB (6633899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d70bbe5b3c9b9eafef2575be2b61361a40411ba90f5b1247b31cac2e9f713a`  
		Last Modified: Tue, 24 Mar 2026 18:40:44 GMT  
		Size: 508.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:c5c96afadb08990519347f2976f090515ebd1de60da307e461c0ef7b09879bd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95dc1468d4fd846dbb34075b55c29a9b3b30bfb1aac8da711dcc6f5a3f972da1`

```dockerfile
```

-	Layers:
	-	`sha256:0da1aa9ca89ff1c5bb794f2fcbadba68c330f91b9d4260426747e50d31ca80aa`  
		Last Modified: Tue, 24 Mar 2026 18:40:44 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:d110573a16f352ba594130e4bf32c526df4189abc0ac1f6c78bd66325c38decd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6355298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7860650d8c0587dd5eaaec925fa3e492f5de9ec04234c36a58b836d4e073b0`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:27 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:27 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:27 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:27 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:27 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c8769a116c1dd3658ea3cb7a85ad34044683b3755f0199ea07aedfb19508216e`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.4 MB (6354789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be47ab573e9b381f4383ec6dff764ee6a2152a6efa67fb3cbad7cddb70140012`  
		Last Modified: Tue, 24 Mar 2026 18:39:31 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:7da25a9c489b921cfe11f5f1acf63d9fa62be21e9c7f917233212318568d2f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f6b05c00b2783cb9b7be7c900f308c52a60f1b7746e33d6640e0a44fe8ab4b0`

```dockerfile
```

-	Layers:
	-	`sha256:f968cd2d36e394bc491931030059cdde8ff1f67a850cd891e1014639762fb1cc`  
		Last Modified: Tue, 24 Mar 2026 18:39:31 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:55a5a2fe6d10d82054a8be63dd23a60bf6ca54f943c5f95dd90fa95b22939f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6346060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9fec07cd77517a0890d58b82b10b9cd98a3dfeb9dd5ccfccbcaeb06d8eb14e`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:22 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:22 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:22 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:22 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:24ef1b2dda251e2e80a3765ff6bd41b920da49a1d3f74d3461d7671772510780`  
		Last Modified: Tue, 24 Mar 2026 15:54:43 GMT  
		Size: 6.3 MB (6345551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae079ec2d754b59a63256322a08a3c465a1d55d7955f74188e809b8671e43ef5`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:8b6db4dd62f0dad26a09cda295ea82eddf0a647d6c1a5950846cfa20927ad8da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7916c7e5fce8cd40ff3f407c7bf121361d1347fa90ee827309bde3c2bbc7bad`

```dockerfile
```

-	Layers:
	-	`sha256:63f7116045a154665c7b2c6481ad137e3bb06b4a0ccf696148737a01d3e87851`  
		Last Modified: Tue, 24 Mar 2026 18:40:26 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:5213658d6dca138e6f31797407757718b10a10de4891bb7fb484fd134f736207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6040752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d8d71244849d512e178b8d1136ad99cf02be5d478fada7f96dabf40c3695e2`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:19 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:19 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:19 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:19 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:19 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:057fcbd8e1788b72b106f31fba3834666e7053d3a22c6cce45486ed3b560cb4e`  
		Last Modified: Tue, 24 Mar 2026 15:54:42 GMT  
		Size: 6.0 MB (6040243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5610d7ed92ff267090e843c22e8840245cc2e521ff205d1e46787750db10dd`  
		Last Modified: Tue, 24 Mar 2026 18:40:23 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:feca932bd8832e50d9f04d35180599c255a8d26d3a2d7a7bf47076aa1e2def06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 KB (10608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690fda93d218169c71a3818ca913b1070d92fcf3feccb1c9e70a808a4f43957c`

```dockerfile
```

-	Layers:
	-	`sha256:28812972c8f2bf701370a8e07053b89868be760e5f968f038dca6d3db19014ac`  
		Last Modified: Tue, 24 Mar 2026 18:40:23 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; ppc64le

```console
$ docker pull nats@sha256:868a9c073cef51edd53ea6544d88a4b91382556753f9b446c53e0469a6c12d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6090986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b516bc45dcd3eb38bf037b1874abfd7a2431030c4a00af2651e4d6ce40b421a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:40:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:40:23 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:40:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:40:25 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:40:25 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:c133b6dba189d986efb270c680d6a9059b370924a73ef6faeadbac5656ea2e42`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.1 MB (6090477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24501ccf50cabbc4d7fb894b237b845ea9ba1dd0a260e42484684c36ab36911`  
		Last Modified: Tue, 24 Mar 2026 18:40:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:21b73621ed19df41f4ad0341c6c169095c90a5720fc090d92f2e93a9517539d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 KB (10513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c483a4e32dfdd8c4fe443ef35f3f30e969de2ce0efb2ac0f27ca86d0d677df`

```dockerfile
```

-	Layers:
	-	`sha256:d480ba93b92b589e975889caf881683a6bca9dc1331219f38e949b0205ead85a`  
		Last Modified: Tue, 24 Mar 2026 18:40:35 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-scratch` - linux; s390x

```console
$ docker pull nats@sha256:982aa85380416c97ebd417c29da6d1ad1208cd7c3e27b34605112b7a559a1fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6473946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b06b9f9f2821602d419bf01a9d908bc9e321facf9f97064f6b4fd3e9e01296`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Tue, 24 Mar 2026 18:39:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Tue, 24 Mar 2026 18:39:13 GMT
COPY /usr/local/bin/nats-server /nats-server # buildkit
# Tue, 24 Mar 2026 18:39:13 GMT
COPY nats-server.conf /nats-server.conf # buildkit
# Tue, 24 Mar 2026 18:39:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 24 Mar 2026 18:39:13 GMT
ENTRYPOINT ["/nats-server"]
# Tue, 24 Mar 2026 18:39:13 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:1f79a2823a9a4a1c9860dbf1223c351eac1ab83f370625f1adcec75b4ad5de05`  
		Last Modified: Tue, 24 Mar 2026 15:54:46 GMT  
		Size: 6.5 MB (6473437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa885b4ccb018e60e0ad65a09e866cfb1c4bd6e1e9ef98a29ba7a2ae81292140`  
		Last Modified: Tue, 24 Mar 2026 18:39:20 GMT  
		Size: 509.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-scratch` - unknown; unknown

```console
$ docker pull nats@sha256:af2f6102c3a54f174244e5e56b25d65a8a5bb089e4dc67ba4b6c349211156dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1c5a0671114bd3ed1f383ec5e1d7c12373209e60676cb1163cbf9224953a29`

```dockerfile
```

-	Layers:
	-	`sha256:5718cb043e8fad6279a100cba1162a5021686eb9a6ccd59c050de52818334e41`  
		Last Modified: Tue, 24 Mar 2026 18:39:20 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json
