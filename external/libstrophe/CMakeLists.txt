set(LIBSTROPHE_SRC
  src/auth.c
  src/conn.c
  src/ctx.c
  src/event.c
  src/handler.c
  src/hash.c
  src/jid.c
  src/md5.c
  src/oocontext.cpp
  src/oostanza.cpp
  src/parser_libxml2.c
  src/sasl.c
  src/sha1.c
  src/snprintf.c
  src/sock.c
  src/stanza.c
  src/thread.c
  src/tls_dummy.c
  src/util.c
)

include_directories(
  ..
)

add_library(libstrophe STATIC
  ${LIBSTROPHE_SRC}
)

set_target_properties(libstrophe
    PROPERTIES
    ARCHIVE_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/lib"
    LIBRARY_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/lib"
)
