## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:ab41660e813c337788470adabc9bdc83014a9a838591b5a84e2bea5420dfff0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:d80de5fb0b681e20ec4639fa4f833fe0b2ba22debc1be07411e80f39c8378592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75905011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bfd8adc999d9645747e81838530954dcc7416818771d3f40743b7298ae567fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 28 Oct 2024 16:40:55 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 16:40:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENV KAPACITOR_VERSION=1.7.6
# Mon, 28 Oct 2024 16:40:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 28 Oct 2024 16:40:55 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 28 Oct 2024 16:40:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 16:40:55 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb66ce059e2c58cd1bca56470e6a25e8e94d630ab09f2c0cc3141d879c460143`  
		Last Modified: Sat, 15 Feb 2025 00:26:38 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff82a75234ac7a2c67a34f6e7192f115d5e12e206035e59917e47237ca12cae`  
		Last Modified: Sat, 15 Feb 2025 00:26:38 GMT  
		Size: 296.5 KB (296501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f13695363bccb9f665399c139ff913d5a2ed7e4ee6208ef774f829ea457c6c`  
		Last Modified: Sat, 15 Feb 2025 00:26:43 GMT  
		Size: 72.0 MB (71980833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667ef208e5bab47062223cab49f2e19071361ea8eedad28a206903e51d10b243`  
		Last Modified: Sat, 15 Feb 2025 00:26:38 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f630e2ff04bbb88b3e31e88074207828bdf03061654955964de05e394c36e557`  
		Last Modified: Sat, 15 Feb 2025 00:26:39 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:7739053a142992f3b94e50635d0eb198c83110a26140d4b75852ba1ce0c51c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.0 KB (384016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590c2694bf70026c8fa8dd67c50dfb9bfa11d0c679791667a23ac1ff5db64258`

```dockerfile
```

-	Layers:
	-	`sha256:584b24fbdeb04a9522b2ac6b8dcd6834cd4ed8406d9f9d3c986d800cc727731d`  
		Last Modified: Fri, 14 Feb 2025 23:21:21 GMT  
		Size: 368.3 KB (368333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b16553670a0a3cb59971f6f10e1686b74c1a3804c0b81eb3d9860df537a4c177`  
		Last Modified: Fri, 14 Feb 2025 23:21:22 GMT  
		Size: 15.7 KB (15683 bytes)  
		MIME: application/vnd.in-toto+json
