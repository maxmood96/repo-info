## `sapmachine:11-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:ae6e783d1993476a575103bff9899938559b426a0d4f7f5f13e67dc17793619c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:ebd47c7c2713d8193f5bbbddeb77f768dd69ff122d8a481fd2558bbbb39a972f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78025628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c13782704874ba7dc7a4864e5911c876e7e2b5181ea582b55d39362607314d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:36:28 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.30 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:36:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 17 Feb 2026 20:36:28 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d942ded37e58f8f39d6516ae93621361758e1666b389a7e9313990963986b69`  
		Last Modified: Tue, 17 Feb 2026 20:36:40 GMT  
		Size: 48.5 MB (48488262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1d2efb7527ae0df451d2de11a73a9aeb57a2e10d486bb47bc0f1a8f7cea9ca8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c906a81c95ec4178b294711f9be3a66b9923fd420586b242a2cfa86bef29a946`

```dockerfile
```

-	Layers:
	-	`sha256:d775032df43c23f23bb3347a5b165f6d014e85ba256838010648d9b2249df320`  
		Last Modified: Tue, 17 Feb 2026 20:36:39 GMT  
		Size: 2.3 MB (2299130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00ceed69977257637f1dafcfd3eddc4809e784b11687197321bbf403f6cc7dfb`  
		Last Modified: Tue, 17 Feb 2026 20:36:39 GMT  
		Size: 8.9 KB (8885 bytes)  
		MIME: application/vnd.in-toto+json
