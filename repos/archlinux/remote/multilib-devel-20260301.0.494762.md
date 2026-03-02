## `archlinux:multilib-devel-20260301.0.494762`

```console
$ docker pull archlinux@sha256:20ac0dba3c5282241f7703467533357379f56160d8d3e682c09115675c8e0493
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20260301.0.494762` - linux; amd64

```console
$ docker pull archlinux@sha256:c84b6ac73dc84aaf21d13e6081b2bd84fffb7d926b9682ab1d101d3afe0a4df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.1 MB (268087964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf7fcd005a84c65d46fd0648d9705ae334ab7abebfae39785ad51a30ee5b7e1`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 02 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 02 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 02 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 02 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 02 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 02 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 02 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 02 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.version=20260301.0.494762
# Mon, 02 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 02 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.created=2026-03-01T00:06:43+00:00
# Mon, 02 Mar 2026 19:13:06 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 19:13:12 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260301.0.494762' /etc/os-release # buildkit
# Mon, 02 Mar 2026 19:13:12 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 19:13:12 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:8c764f1514a66c73f29af53aaf52d5a38e20996ec1ad72fa0c732d08486ac2fb`  
		Last Modified: Mon, 02 Mar 2026 19:13:59 GMT  
		Size: 268.1 MB (268077638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b339c3bbac1bb41286ebb0486af34c2333afecbebc5998d81f90cdf7bb5846`  
		Last Modified: Mon, 02 Mar 2026 19:13:53 GMT  
		Size: 10.3 KB (10326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20260301.0.494762` - unknown; unknown

```console
$ docker pull archlinux@sha256:3d1cfb9d9984c251cb56556fa82a087255821a7c5ebf24eb14ef74de3ea912ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 MB (12520926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d109be139ec9b0f8830309ffc5781c6d9416ebc602a02e41cc91cade6752699e`

```dockerfile
```

-	Layers:
	-	`sha256:b3105912f0b710d34ede0d4f3b7ecd0d8058497e528861e68e0f9fc43b35fb84`  
		Last Modified: Mon, 02 Mar 2026 19:13:54 GMT  
		Size: 12.5 MB (12509159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1751276bc1904666d9615e22dc7e3a792fe85be43d05a3cd3eeec837c816152`  
		Last Modified: Mon, 02 Mar 2026 19:13:53 GMT  
		Size: 11.8 KB (11767 bytes)  
		MIME: application/vnd.in-toto+json
