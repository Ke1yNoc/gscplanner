AUTOMAKE_OPTIONS = foreign

AM_CPPFLAGS = -I../.. -I/usr/local/opt/openssl/include

AM_LDFLAGS = -L/usr/local/opt/openssl/lib

bin_PROGRAMS = psr_server test_psr_solver setup_problem minlp_planning make_viewer_json

psr_server_SOURCES = PsrParserPlugin.h PsrParserPlugin.cc PsrSolver.h PsrSolver.cc utility.h utility.cc psr_server.cc 

psr_server_LDADD = -lSgtCore -larmadillo -lyaml-cpp -lPowerTools++ -lipopt -lcoinhsl -lklu -lamd -lbtf -lcolamd $(GUROBI_LIBS) $(BONMIN_LIBS) -lcpprest -lcrypto -lssl $(BOOST_DATE_TIME_LIB) $(BOOST_CHRONO_LIB) $(BOOST_FILESYSTEM_LIB) $(BOOST_REGEX_LIB) $(BOOST_SYSTEM_LIB) $(BOOST_THREAD_LIB) $(EXTRA_LIBS)

psr_server_CFLAGS = $(AM_CFLAGS)

test_psr_solver_SOURCES = PsrParserPlugin.h PsrParserPlugin.cc PsrSolver.h PsrSolver.cc utility.h utility.cc test_psr_solver.cc

test_psr_solver_LDADD = -lSgtCore -larmadillo -lyaml-cpp -lPowerTools++ -lipopt -lcoinhsl -lklu -lamd -lbtf -lcolamd $(GUROBI_LIBS) $(BONMIN_LIBS) -lcpprest -lcrypto -lssl $(BOOST_DATE_TIME_LIB) $(BOOST_CHRONO_LIB) $(BOOST_FILESYSTEM_LIB) $(BOOST_REGEX_LIB) $(BOOST_SYSTEM_LIB) $(BOOST_THREAD_LIB) $(EXTRA_LIBS)

setup_problem_SOURCES = PsrSolver.h PsrSolver.cc utility.h utility.cc setup_problem.cc

setup_problem_LDADD = -lSgtCore -larmadillo -lyaml-cpp -lPowerTools++ -lipopt -lcoinhsl -lklu -lamd -lbtf -lcolamd $(GUROBI_LIBS) $(BONMIN_LIBS) -lcpprest -lcrypto -lssl $(BOOST_DATE_TIME_LIB) $(BOOST_CHRONO_LIB) $(BOOST_FILESYSTEM_LIB) $(BOOST_REGEX_LIB) $(BOOST_SYSTEM_LIB) $(BOOST_THREAD_LIB) $(EXTRA_LIBS)

setup_problem_CFLAGS = $(AM_CFLAGS)

minlp_planning_SOURCES = PsrParserPlugin.h PsrParserPlugin.cc PsrSolver.h PsrSolver.cc utility.h utility.cc minlp_planning.cc

minlp_planning_LDADD = -lSgtCore -larmadillo -lyaml-cpp -lPowerTools++ -lipopt -lcoinhsl -lklu -lamd -lbtf -lcolamd $(GUROBI_LIBS) $(BONMIN_LIBS) -lcpprest -lcrypto -lssl $(BOOST_DATE_TIME_LIB) $(BOOST_CHRONO_LIB) $(BOOST_FILESYSTEM_LIB) $(BOOST_REGEX_LIB) $(BOOST_SYSTEM_LIB) $(BOOST_THREAD_LIB) $(EXTRA_LIBS)

minlp_planning_CFLAGS = $(AM_CFLAGS)

make_viewer_json_SOURCES = PsrParserPlugin.h PsrParserPlugin.cc PsrSolver.h PsrSolver.cc ViewerJson.h ViewerJson.cc utility.h utility.cc make_viewer_json.cc

make_viewer_json_LDADD = -lSgtCore -larmadillo -lyaml-cpp -lPowerTools++ -lipopt -lcoinhsl -lklu -lamd -lbtf -lcolamd $(GUROBI_LIBS) $(BONMIN_LIBS) -lcpprest -lcrypto -lssl $(BOOST_DATE_TIME_LIB) $(BOOST_CHRONO_LIB) $(BOOST_FILESYSTEM_LIB) $(BOOST_REGEX_LIB) $(BOOST_SYSTEM_LIB) $(BOOST_THREAD_LIB) $(EXTRA_LIBS)

make_viewer_json_CFLAGS = $(AM_CFLAGS)


lib_LTLIBRARIES = libpsr.la

libpsr_la_SOURCES = psr_ext_solver.h psr_ext_solver.cc popfExternalSolver.h

libpsr_la_LIBADD = -lcpprest -lcrypto -lssl $(BOOST_REGEX_LIB) $(EXTRA_LIBS)

libpsr_la_CPPFLAGS = $(AM_CPPFLAGS)
