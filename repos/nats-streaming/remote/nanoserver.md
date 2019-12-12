## `nats-streaming:nanoserver`

```console
$ docker pull nats-streaming@sha256:adf209b72e0cd47d09f30fcdeaf9a8dfe59a14d6df4ec6dd58e114899e879071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17134.1184; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17134.1184; amd64

```console
$ docker pull nats-streaming@sha256:f71b8c9579a7a42b1e7b3d8e718274739ca7d692f2aa8bba55de21515a15bb08
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158738143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd886ef6b5ff5b0e5be848489bdf1b5db0bccc8d26a57009941c48b4a727414f`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 11 Apr 2018 22:12:30 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:03:29 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 18:28:28 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 22:50:49 GMT
RUN cmd /S /C #(nop) WORKDIR C:\nats-streaming-server
# Wed, 11 Dec 2019 22:50:52 GMT
RUN cmd /S /C #(nop) COPY file:d333dfb9aa0fca02ce2e2300447082af645803b49703ee1671951f7dba266042 in nats-streaming-server.exe 
# Wed, 11 Dec 2019 22:50:54 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 11 Dec 2019 22:50:55 GMT
RUN cmd /S /C #(nop)  CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:e46172273a4e4384e1eec7fb01091c828a256ea0f87b30f61381fba9bc511371`  
		Last Modified: Mon, 17 Sep 2018 20:23:30 GMT  
		Size: 92.8 MB (92818888 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0a1fd0c25c533d146f34b62fccd2324eeb48fb1ff715bd943497309a9718102d`  
		Size: 60.4 MB (60405616 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fedec297525cf00361caff642c6e2ccdf40638f2636bb8fedb8b119b7527bb6f`  
		Last Modified: Wed, 11 Dec 2019 18:34:13 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b385a4ce665544f02602cd323d1fb14b060c7d43e3568f52f8ee2ce37f35351e`  
		Last Modified: Wed, 11 Dec 2019 22:51:55 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e55887cbfe81767eb5578349cc3381c4c86ea810adba04eeebb204ba8c6b2e5`  
		Last Modified: Wed, 11 Dec 2019 22:51:57 GMT  
		Size: 5.5 MB (5509679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398b33543ead5f6e66cd4c2a6b88633df3495d61a1744d7433335e7ce35e83d3`  
		Last Modified: Wed, 11 Dec 2019 22:51:55 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63c5077d299b3ef63785823d022786aba09d722e64dfb8871f5203686ff876c`  
		Last Modified: Wed, 11 Dec 2019 22:51:55 GMT  
		Size: 922.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
