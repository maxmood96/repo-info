## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:a1a1c99131ac48969fb0fa77bc7c0b3728bbdf54c52203a551fc287a7bdaf72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:7a94cf61f1b30957d82adf2dd042de50945227f8037ac73678429c317aafd652
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22304983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7bb2ca838606bf3dfd404941ee586e450f867d29967ce61154bf26514f42f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:12:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:12:40 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Tue, 10 Aug 2021 23:20:54 GMT
ENV CHRONOGRAF_VERSION=1.8.9
# Tue, 10 Aug 2021 23:21:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Tue, 10 Aug 2021 23:21:00 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 10 Aug 2021 23:21:01 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 10 Aug 2021 23:21:01 GMT
EXPOSE 8888
# Tue, 10 Aug 2021 23:21:01 GMT
VOLUME [/var/lib/chronograf]
# Tue, 10 Aug 2021 23:21:01 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Tue, 10 Aug 2021 23:21:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 10 Aug 2021 23:21:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4496f95da0ff203c55ba4ff45e6cc518bfd24507a21516931244d25e8db7d14`  
		Last Modified: Wed, 14 Apr 2021 20:13:37 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9162e7666a3906b38fdfed2592cc2e4df967e365a3fcf17c8d6320caed7fd960`  
		Last Modified: Wed, 14 Apr 2021 20:13:33 GMT  
		Size: 280.9 KB (280875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6315189d9256b1aa5058b260d261730d26e945034678c5ea970e6b3ac7dd6c04`  
		Last Modified: Tue, 10 Aug 2021 23:22:39 GMT  
		Size: 19.2 MB (19198985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9cc663516dc172d4e68e80a286098bb18a9606720074804efced99c9e628db8`  
		Last Modified: Tue, 10 Aug 2021 23:22:36 GMT  
		Size: 12.3 KB (12266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ecb5c127e90f14d323086d290be04bf911cc6a0f2d59500604058747dd2291`  
		Last Modified: Tue, 10 Aug 2021 23:22:36 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9108f10fb89a41c0eed8a2222be8bb67cf30d4d0cf1bf36500f5d4b9ca4f210`  
		Last Modified: Tue, 10 Aug 2021 23:22:36 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
