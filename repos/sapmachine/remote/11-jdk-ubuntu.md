## `sapmachine:11-jdk-ubuntu`

```console
$ docker pull sapmachine@sha256:5c83d7194c0598ef6116a46a5f2c7b60658f9899e8eaae9c81afcfdf5f3518ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jdk-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:d70512b7a5b985a3a5ea142c2951676af22ec2ebea9e1f417ac164250eb7102e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.4 MB (233430134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4f1aebebb07f1a436ddee4d22e293c1f04ebe77ce9ade9f33cb65d006088b0`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:16 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:16 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:16 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 15 Jul 2025 19:58:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.28 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 15 Jul 2025 19:58:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d09b111e101c22aa24c8a058789b8efb1932664fd64f0aee2509289def91552`  
		Last Modified: Thu, 02 Oct 2025 10:05:34 GMT  
		Size: 203.7 MB (203707123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b23ec90e2bbbca252e752023a10ae4213b4d12a3bcc04614299aa21e78894ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c03be0b02b9889b038655cd3b3b52bbdcec4c5c3cbdb61de6008e1412bdba62`

```dockerfile
```

-	Layers:
	-	`sha256:d037786f36506318551a0100f0850e725aaf33ead9e5d77160d966f5ea01bd33`  
		Last Modified: Thu, 02 Oct 2025 09:04:16 GMT  
		Size: 2.6 MB (2615590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e8cffd1aea9c941902effceae6d6ade67647ecfc49bb509bce9b91db7a2980d`  
		Last Modified: Thu, 02 Oct 2025 09:04:17 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json
