## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:d799192a2322be6343aa9f363a5ffcffc4a66e0efd1b704496e6f2000ccc3759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:94f3ea894258737da30c481fca4b3d828c628bec06bc661104352a066b7b2a2d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62916986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b952124249b746f7d2be4bdbd4a11e424ee8477a2da647de7db88f876bc18ddf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:22:28 GMT
ADD file:49aaad883f9932e76df5604c9353bdbc51cd2c74b986b57b2dbb4f3aeaa46404 in / 
# Tue, 09 Jun 2020 01:22:28 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 08:07:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 08:07:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 09 Jun 2020 08:07:10 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 09 Jun 2020 08:07:17 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 08:07:26 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:516091449b2853b301713d61c7a73bfbe7ae63ace598e76e1d5e9da246f88b37`  
		Last Modified: Tue, 09 Jun 2020 01:27:16 GMT  
		Size: 51.5 MB (51526780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2f581808a058630ee4fec35edcfee2c78a49f00382bea772d272a3e9cb9fa8`  
		Last Modified: Tue, 09 Jun 2020 08:08:51 GMT  
		Size: 11.1 MB (11088475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c614cb3fcf9fca507e0d41cdec2104f78bcc60cef805cbcae2b08e3c36674ba2`  
		Last Modified: Tue, 09 Jun 2020 08:08:49 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b37da63e874923397bd47369d99e4277ba31f376837b25f8a0ee14afb8a0722`  
		Last Modified: Tue, 09 Jun 2020 08:08:49 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:affd8afb9c00204af08b48652609186e3072a7d4df44528341d0273888d5bb19`  
		Last Modified: Tue, 09 Jun 2020 08:08:49 GMT  
		Size: 299.4 KB (299411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af3adbb544dc38b4b2cdc5b4c8e1f0dce62df8c90289649a35816cda6f63060`  
		Last Modified: Tue, 09 Jun 2020 08:08:55 GMT  
		Size: 318.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
