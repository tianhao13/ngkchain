+++
title = "`void outcome_throw_as_system_error_with_payload(BoostErrorCodeEnum &&)`"
description = "Specialisation of `outcome_throw_as_system_error_with_payload()` for input types where `boost::system::errc::is_error_code_enum<BoostErrorCodeEnum>` or `boost::system::errc::is_error_condition_enum<BoostErrorCodeEnum>` is true."
+++

A specialisation of `outcome_throw_as_system_error_with_payload()` for types where `boost::system::errc::is_error_code_enum<BoostErrorCodeEnum>` or `boost::system::errc::is_error_condition_enum<BoostErrorCodeEnum>` is true. This executes {{% api "OUTCOME_THROW_EXCEPTION(expr)" %}} with a `boost::system::system_error` constructed from the result of the ADL discovered free function `make_error_code(BoostErrorCodeEnum)`.

*Overridable*: Argument dependent lookup.

*Requires*: Either `boost::system::errc::is_error_code_enum<T>` or `boost::system::errc::is_error_condition_enum<T>` to be true for a decayed `BoostErrorCodeEnum`.

*Namespace*: `boost::system`

*Header*: `<outcome/boost_result.hpp>`
