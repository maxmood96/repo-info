## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:6c12933348b309e2808986ba2543e0245d0302f5dd843fcd47dfa586c821e05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:f4ba86d4c118865b456c019d23ae2fb7467076a94012f7ab5a8baa5d366943c0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61428135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c30dcf261eb34ed7ba953188683d6cf85e2a41d3984cc4082f743b775478f105`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Thu, 16 Sep 2021 21:20:06 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 30 Sep 2021 18:21:29 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 30 Sep 2021 18:21:58 GMT
ENV KAPACITOR_VERSION=1.6.2
# Thu, 30 Sep 2021 18:22:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 30 Sep 2021 18:22:11 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 30 Sep 2021 18:22:11 GMT
EXPOSE 9092
# Thu, 30 Sep 2021 18:22:11 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 30 Sep 2021 18:22:12 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Thu, 30 Sep 2021 18:22:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 30 Sep 2021 18:22:12 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8cf55ffd68f3512245522356168367182cfdaeb0a0d11bbd5328472d4c0761`  
		Last Modified: Thu, 16 Sep 2021 21:24:04 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35128f89929d86c35c1dfabaaea2552df6e9c25e7ec0d08e798390d47c11a85b`  
		Last Modified: Thu, 30 Sep 2021 18:22:31 GMT  
		Size: 281.5 KB (281501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a9bcd86c1c04ecaf75b22654e5cf8e5c6b44f7ab70bafbc7d474adfa252eaa`  
		Last Modified: Thu, 30 Sep 2021 18:23:14 GMT  
		Size: 58.3 MB (58331557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a1340b55624bc8a778568b36dfcc297ad4dba03b63cb000ac7d00f0de5a3fb`  
		Last Modified: Thu, 30 Sep 2021 18:23:06 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e61b33e2e928b59c5980ead89d66337a0acd23fcbbda69e7491c754ad579ead`  
		Last Modified: Thu, 30 Sep 2021 18:23:06 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
