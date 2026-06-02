## `sapmachine:25-jre`

```console
$ docker pull sapmachine@sha256:69491d88e0eb10a24408d09ae9cf49bc6af6cb1f3d23036e21d200c3eb63e0c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-jre` - linux; amd64

```console
$ docker pull sapmachine@sha256:377cc2a91338a4b3b87eb53ab933f701c737f9e52f4c4aa8299c9808eae752b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87805898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd8d163ce9eb30ac795e0eebdddc7c5dd278ebd0ac370db66a7778a28ee1ba7a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:24:09 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:24:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 02 Jun 2026 08:24:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ac6faf49dd8779c2e919a2a5dd6f2c34598c7eabf8c2c17c3be73ddd839b88`  
		Last Modified: Tue, 02 Jun 2026 08:24:22 GMT  
		Size: 58.1 MB (58073093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:50c69163c8ad9aeac42b166f30b08afc268a8a1beab39ff7f2a356af6c1379e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2538852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cffa5a3a818cba2f51b178dfd4097d3504de683610f0c880155beb87d9596c5`

```dockerfile
```

-	Layers:
	-	`sha256:863fef5271492b06778e6da1a246519d992a624971e5b01e35617627107f3067`  
		Last Modified: Tue, 02 Jun 2026 08:24:21 GMT  
		Size: 2.5 MB (2527826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09b4bd3abd249a0430734479ddf499fab62231f40de70260145986dbf296f0ed`  
		Last Modified: Tue, 02 Jun 2026 08:24:21 GMT  
		Size: 11.0 KB (11026 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jre` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:4f8c239ee72e976676e774a59b4923158f6dd9641dce3e48666cefcbd2c1fdbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.9 MB (85918930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88d63a5beca333f720fbe802de3be6f5843a731a8696a3258c7c2f97bfb7613`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:24:17 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:24:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 02 Jun 2026 08:24:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3b39d6a93df8c89e02a172f7736775f886e392479b17e2d73006278e9914a1`  
		Last Modified: Tue, 02 Jun 2026 08:24:30 GMT  
		Size: 57.0 MB (57042524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:81ec4036f6a6621aa0054ac209aaae373f5fbfbea82d7aa569f0d5889506e775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2539589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4a158088ef1b5b52ff6ec600342dfd2da503b0ded0e3e87fe5d4b5bb772c8c`

```dockerfile
```

-	Layers:
	-	`sha256:fc7d5163bdbf8174a3805042e5f1cb06451a5723f5de055c9d4d443141c9ece0`  
		Last Modified: Tue, 02 Jun 2026 08:24:29 GMT  
		Size: 2.5 MB (2528375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a13670051f95475a279c207d0e2fd8d5a757197e2827b8d3960d004a482cc0c`  
		Last Modified: Tue, 02 Jun 2026 08:24:28 GMT  
		Size: 11.2 KB (11214 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jre` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:35390371ba36aad7bd86e1fe511cbfff6003988db628d0af4a64edd8617e6b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93263076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe36e3350df454bdbb9a234e4e4ab87aa15d183c5a34d79a0411fdb3d192e33`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:55:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:55:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 02 Jun 2026 08:55:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8956de05789d972a01c8a4907fb9209d2abf1824e3f3c79c947fbecd52bd5fa4`  
		Last Modified: Tue, 02 Jun 2026 08:56:32 GMT  
		Size: 58.9 MB (58948977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ecb6aa4c913c60fbf42a416774160ecc517a879676ae9d29b74431fc475b672e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2537825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797a2c2cfda034417b54d1396752597e82f5735ea5a5c4316422bd213b0c0516`

```dockerfile
```

-	Layers:
	-	`sha256:dbc092afcd9979f45b3970a8a90979c8e667663340e9ab7af6183f3060f3f6a7`  
		Last Modified: Tue, 02 Jun 2026 08:56:31 GMT  
		Size: 2.5 MB (2526712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:642b4e9fd728b8f87ae8be785977195a5bc0ec793c2a49dce496a1d71dc586b7`  
		Last Modified: Tue, 02 Jun 2026 08:56:30 GMT  
		Size: 11.1 KB (11113 bytes)  
		MIME: application/vnd.in-toto+json
